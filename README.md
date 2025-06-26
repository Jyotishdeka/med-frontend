project:
  name: SmartMedicare Frontend
  description: |
    This is the frontend React.js project for the SmartMedicare application — an online medicine ordering and doctor consultation platform. The backend is powered by Strapi, and API interactions are managed using Axios.

tech_stack:
  - React.js (Vite)
  - Tailwind CSS
  - Redux Toolkit
  - React Router DOM v6
  - Axios
  - Strapi (Headless CMS)
  - AI Prescription Validation Service

folder_structure:
  src:
    - assets: "Images, icons, fonts"
    - components:
        - common: "Generic shared components"
    - features:
        - auth: "Auth feature (login, signup)"
        - medicines: "Medicine listing, ordering"
    - layouts: "Layout components"
    - pages: "Route-level components"
    - services: "Axios setup and API utilities"
    - hooks: "Custom React hooks"
    - store: "Redux store configuration"
    - utils: "Helper functions"
    - constants: "Constant values"
    - styles: "Tailwind and global styles"
    - App.jsx: "Main App component"
    - main.jsx: "Entry point"
    - routes.jsx: "All route definitions"

setup:
  clone:
    - git clone https://github.com/your-org/smartmedicare-frontend.git
    - cd smartmedicare-frontend
  install: npm install
  environment:
    file: .env
    variables:
      - VITE_API_BASE_URL=http://localhost:1337/api
  run: npm run dev
  preview_url: http://localhost:5173

scripts:
  - command: npm run dev
    description: Run development server
  - command: npm run build
    description: Build for production
  - command: npm run preview
    description: Preview production build
  - command: npm run lint
    description: Lint the project

contributing_guide:
  - Work only within your assigned feature folder inside `src/features/`.
  - Use Axios from `services/axiosInstance.js`.
  - Reusable components go in `components/common/`.
  - Use Tailwind CSS for styling.
  - Do not push to main branch directly. Create a feature branch and raise a pull request.

axios_usage_example: |
  import axiosInstance from '@/services/axiosInstance';

  const fetchMedicines = async () => {
    const res = await axiosInstance.get('/medicines');
    return res.data;
  };

tips:
  - Use `useSelector` and `useDispatch` for Redux state.
  - Break down pages into small components.
  - Keep API and state logic inside feature folders.

authors:
  project_lead: Your Name
  interns:
    - Intern 1
    - Intern 2
    - Intern 3

license: MIT © Your Company Name
