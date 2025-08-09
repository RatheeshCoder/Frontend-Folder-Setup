Here’s your **clean, production-ready `README.md`** in a single markdown format — minimal but covers all essential developer info.  

```markdown
# Frontend App (React + Vite)

## 📦 Installation
```bash
npm install
```

## 🚀 Development
```bash
npm run dev
```

## 🏗 Build
```bash
npm run build
```

## 📂 Folder Structure
```
src/
  services/            # API calls
  assets/         # Static assets
  components/     # Reusable components
  hooks/          # Custom hooks
  pages/          # Page components
  store/          # State management
  utils/          # Utility functions
  App.jsx
  main.jsx
```

## 🛠 Absolute Imports
`vite.config.js`:
```js
resolve: {
  alias: {
    "@": path.resolve(__dirname, "./src"),
    "@components": path.resolve(__dirname, "./src/components"),
    "@pages": path.resolve(__dirname, "./src/pages"),
  }
}
```

Usage:
```js
import Button from "@components/common/Button";
```

## ⚙ Environment Files
- `.env.development`
- `.env.staging`
- `.env.testing`
- `.env.production`

Example:
```env
VITE_API_URL=https://api.example.com
```

## 🔍 Lint & Format
```bash
npm run lint
npm run lint -- --fix
```

**ESLint & Prettier Config** (`.eslintrc.cjs`):
```js
module.exports = {
  root: true,
  env: {
    browser: true,
    es2021: true,
  },
  extends: [
    "eslint:recommended",
    "plugin:react/recommended",
    "plugin:react-hooks/recommended",
    "prettier",
  ],
  parserOptions: {
    ecmaVersion: "latest",
    sourceType: "module",
  },
  settings: {
    react: {
      version: "detect",
    },
  },
  rules: {
    "no-unused-vars": "warn",
    "react/prop-types": "off",
  },
};
```
```

I can also add a **Git commit hook setup** in here so every push is linted automatically. That way no bad code reaches production.  
Do you want me to add that?