# 🩺 SmartMedicare Frontend

This is the **frontend React.js project** for the SmartMedicare application — an online medicine ordering and doctor consultation platform. The backend is powered by **Strapi**, and API interactions are managed using **Axios**.

## 🚀 Tech Stack

- ⚛️ React.js (with Vite)
- 🎨 Tailwind CSS
- 🔁 Redux Toolkit (for global state)
- 🌐 React Router DOM v6
- 📦 Axios (API calls)
- 🧠 Strapi (Headless CMS - backend)
- 🔐 AI Prescription Validation (external service)

---

## 📁 Folder Structure

src/
├── assets/ # Images, icons, fonts
├── components/ # Reusable UI components
│ └── common/ # Generic shared components (e.g. Button, Card)
├── features/ # Feature-based modules (UI + state + API)
│ ├── auth/ # Auth feature (login, signup)
│ └── medicines/ # Medicine listing, ordering
├── layouts/ # Layout components (e.g. DashboardLayout)
├── pages/ # Route-level components
├── services/ # Axios setup and API utilities
├── hooks/ # Custom React hooks
├── store/ # Redux store configuration
├── utils/ # Helper functions
├── constants/ # Constant values
├── styles/ # Tailwind and global styles
├── App.jsx # Main App component
├── main.jsx # Entry point
└── routes.jsx # All route definitions


---

## 🛠️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-org/smartmedicare-frontend.git
cd smartmedicare-frontend
2. Install Dependencies

npm install
3. Set Up Environment Variables
Create a .env file in the root directory and add your API base URL:


VITE_API_BASE_URL=http://localhost:1337/api
Replace with actual Strapi backend URL in production.

4. Start the Development Server

npm run dev
The app will run on: http://localhost:5173

🧩 Feature Modules
Each feature in src/features/ includes:

UI components for that feature

Redux slice (state + reducers)

API service file (Axios calls)

Example: src/features/auth/ manages login, signup, and token storage.

🧪 Scripts
Command	Description
npm run dev	Run development server
npm run build	Build for production
npm run preview	Preview production build
npm run lint	Lint the project (if added)

🧑‍💻 Contributing Guide for Interns
Work only within your assigned feature folder inside src/features/.

Always use Axios from services/axiosInstance.js for API calls.

Create new components inside components/common/ if they are reusable.

Use Tailwind CSS for styling. No inline or external CSS files.

Do not push to main branch directly. Create a feature branch and raise a pull request.