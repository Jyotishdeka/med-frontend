# 🩺 SmartMedicare Frontend

This is the **frontend React.js project** for the SmartMedicare application — an online platform for ordering medicines and booking doctor consultations. The backend is powered by **Strapi**, and we use **Axios** for handling API interactions. The project also integrates an **AI-powered prescription validation service**.

---

## 🔧 Tech Stack

- ⚛️ **React.js** (Vite)
- 🎨 **Tailwind CSS**
- 🧠 **Redux Toolkit**
- 🌐 **React Router DOM v6**
- 📦 **Axios**
- 🗃️ **Strapi** (Headless CMS)
- 🤖 **AI Prescription Validation Service**

---

## 📁 Project Folder Structure

```bash
src/
├── assets/           # Images, icons, fonts
├── components/       # Reusable UI components
│   └── common/       # Generic shared components (Button, Card, etc.)
├── features/         # Feature-based modules (UI + state + API)
│   ├── auth/         # Auth feature (login, signup)
│   └── medicines/    # Medicine listing, ordering
├── layouts/          # Layout components (e.g., DashboardLayout)
├── pages/            # Route-level components
├── services/         # Axios setup and API utilities
├── hooks/            # Custom React hooks
├── store/            # Redux store configuration
├── utils/            # Helper functions
├── constants/        # Constant values and enums
├── styles/           # Tailwind and global styles
├── App.jsx           # Main App component
├── main.jsx          # App entry point
└── routes.jsx        # Route definitions


🚀 Getting Started
1️⃣ Clone the Repository
git clone https://github.com/your-org/smartmedicare-frontend.git
cd smartmedicare-frontend

2️⃣ Install Dependencies
npm install

3️⃣ Setup Environment Variables
Create a .env file in the root folder with the following:

VITE_API_BASE_URL=http://localhost:1337/api
Replace with your actual Strapi backend URL if running in production.

4️⃣ Run the Development Server
npm run dev
Visit: http://localhost:5173

📜 NPM Scripts
Command	Description
npm run dev	Start development server
npm run build	Create production build
npm run preview	Preview production locally
npm run lint	Lint the codebase (optional)

📂 Feature Folder Guidelines
Each feature lives in its own folder under src/features/. This folder contains:

React components for that feature.

Redux slice for state management.

API file for handling backend requests.

Example: src/features/medicines/

MedicinesPage.jsx – UI

medicinesSlice.js – Redux state

medicinesAPI.js – Axios calls

🔗 Axios Usage (Example)
Use the shared axiosInstance from services/axiosInstance.js:

import axiosInstance from '@/services/axiosInstance';

const fetchMedicines = async () => {
  const res = await axiosInstance.get('/medicines');
  return res.data;
};
🤝 Intern Contribution Guidelines
✅ Do:

Work only in your assigned feature folder inside src/features/.

Use the global Axios instance from services/axiosInstance.js.

Place shared components inside components/common/.

Use Tailwind CSS only — no external or inline styles.

Commit to a feature branch and raise a pull request.

🚫 Don’t:

Push directly to the main branch.

Write duplicate components across features.

Leave unused imports or commented code in production commits.

💡 Pro Tips
Use useSelector and useDispatch from Redux Toolkit to manage global state.

Organize your feature code: separate UI, API, and logic.

Use custom hooks from the hooks/ folder when reusable logic is needed.

Keep your components small and focused.

