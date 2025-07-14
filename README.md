# Projects Manager Demo App

A simple React demo application for creating, viewing, and managing projects and their associated tasks. Built with Vite, Tailwind CSS, and ESLint to showcase modern front‑end tooling and React patterns.

---

## Table of Contents

- [Features](#features)  
- [Getting Started](#getting-started)  
- [Concepts Practiced](#concepts-practiced)  
- [What I Learned](#what-i-learned)  
- [License](#license)  

---

## Features

- Create, select, and delete projects  
- Add and remove tasks within each project  
- Form validation with a modal dialog for errors  
- Native `<dialog>` element portaled via ReactDOM  
- Responsive, utility‑first styling with Tailwind CSS  
- Instant development with Vite  

---

## Getting Started

1. **Clone the repo**  
   ```bash
   git clone https://github.com/Peglo98/Projects-Manager.git
   cd Projects-Manager
   ```
2. **Install dependencies**  
   ```bash
   npm install
   ```
3. **Run in development mode**  
   ```bash
   npm run dev
   ```
4. **Build for production**  
   ```bash
   npm run build
   ```

---

## Concepts Practiced

- **React Functional Components & Props**  
  Splitting UI into small, reusable components (e.g. `NewProject`, `ProjectsSidebar`, `SelectedProject`, `Tasks`, etc.)  
- **React Hooks**  
  - `useState` for local state in both parent (`App.jsx`) and child (`NewTask.jsx`) components  
  - `useRef` for uncontrolled form inputs and imperatively controlling the native `<dialog>` element  
  - `useImperativeHandle` combined with `forwardRef`‑style patterns to expose an `open()` method on the `Modal` component  
- **Portals & Native `<dialog>`**  
  Rendering the modal into a separate DOM node (`#modal-root`) using `createPortal`  
- **Controlled vs. Uncontrolled Inputs**  
  - Controlled example in `NewTask.jsx` via `useState` and `onChange`  
  - Uncontrolled example in `NewProject.jsx` via `useRef` on `<Input />` fields  
- **Array Rendering & Conditional Styling**  
  Mapping over projects and tasks, applying dynamic Tailwind classes based on selection state  
- **JavaScript Date Formatting**  
  Localizing the project due date display with `toLocaleDateString("pl-PL", {...})`  
- **Styling with Tailwind CSS**  
  Utility‑first classes for layout, spacing, and responsive design  
- **Development Tooling**  
  - Bundler and dev server with Vite (`vite.config.js`)  
  - Linting with ESLint and React hooks rules (see `package.json`)  
  - PostCSS autoprefixer and Tailwind integration (`postcss.config.js`)  

---

## License

This project is licensed under the MIT License.  
