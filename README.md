

```markdown
# Frontend Folder Setup (React + Vite)

A production-ready **React 19 + Vite 7** starter template with professional folder structure, absolute imports, ESLint configuration, and multi-environment support.

---

## 🚀 Features
- **React 19** with Vite for fast builds
- **Environment Variables** for `development`, `staging`, `testing`, and `production`
- **Absolute Imports** using aliases (`@components`, `@pages`, etc.)
- **ESLint** configured for best practices
- **Optimized Folder Structure** for scalability
- **Ready for Production Builds**

---

## 📂 Folder Structure
```

frontend-folder-setup/
├── public/                     # Static assets (served as-is)
├── src/
│   ├── api/                     # API call functions
│   ├── assets/                  # Images, fonts, icons
│   ├── components/
│   │   ├── common/              # Shared reusable components
│   │   └── layout/              # Layout components (Header, Footer)
│   ├── config/                  # App configurations & env loader
│   ├── hooks/                   # Custom React hooks
│   ├── pages/                   # Page-level components
│   ├── store/                   # State management (Redux/Zustand)
│   ├── utils/                   # Helper functions
│   ├── App.jsx                  # Root App component
│   └── main.jsx                 # Entry point
├── .env.development             # Development environment variables
├── .env.staging                 # Staging environment variables
├── .env.test                    # Testing environment variables
├── .env.production              # Production environment variables
├── vite.config.js               # Vite configuration with aliases
├── package.json
├── eslint.config.js             # ESLint configuration
└── README.md

````

---

## 🌍 Environment Variables

Create separate `.env` files in the root:

**`.env.development`**
```env
VITE_API_URL=https://dev.api.example.com
VITE_APP_NAME=MyApp (Dev)
````

**`.env.staging`**

```env
VITE_API_URL=https://staging.api.example.com
VITE_APP_NAME=MyApp (Staging)
```

**`.env.test`**

```env
VITE_API_URL=https://test.api.example.com
VITE_APP_NAME=MyApp (Test)
```

**`.env.production`**

```env
VITE_API_URL=https://api.example.com
VITE_APP_NAME=MyApp
```

📌 **Note:**
All environment variables **must** start with `VITE_` for Vite to expose them in your code.

---

## 🛠 Aliases (Absolute Imports)

Aliases are configured in `vite.config.js`:

```javascript
resolve: {
  alias: {
    "@": path.resolve(__dirname, "./src"),
    "@components": path.resolve(__dirname, "./src/components"),
    "@pages": path.resolve(__dirname, "./src/pages"),
    "@assets": path.resolve(__dirname, "./src/assets"),
    "@api": path.resolve(__dirname, "./src/api"),
    "@store": path.resolve(__dirname, "./src/store"),
    "@utils": path.resolve(__dirname, "./src/utils"),
    "@hooks": path.resolve(__dirname, "./src/hooks"),
    "@config": path.resolve(__dirname, "./src/config"),
  }
}
```

**Example Usage:**

```javascript
import Button from "@components/common/Button.jsx";
import { fetchUser } from "@api/user.js";
```

---

## 📦 Install Dependencies

```bash
npm install
```

---

## 🏃 Run Development Server

```bash
npm run dev
```

Server will start at: [http://localhost:5173](http://localhost:5173)

---

## 🏗 Build for Production

```bash
npm run build
```

The production-ready files will be in the `dist/` directory.

---

## 👀 Preview Production Build

```bash
npm run preview
```

---

## 🧹 Lint & Fix Code

```bash
npm run lint
npm run lint -- --fix
```

---

## 🧪 Testing (Optional if vitest/jest added)

```bash
npm run test
```

---

## 🤝 Contribution Guidelines

1. **Fork** the repository
2. Create a **feature branch**

   ```bash
   git checkout -b feature/my-feature
   ```
3. Commit your changes

   ```bash
   git commit -m "feat: add new component"
   ```
4. Push to your branch

   ```bash
   git push origin feature/my-feature
   ```
5. Open a **Pull Request**

---

## 📜 License

This project is licensed under the MIT License.

---

## 💡 Tips

* Always restart Vite after changing aliases in `vite.config.js`.
* Use `.env` files to separate configurations for each environment.
* Use `@` imports to keep your imports clean and maintainable.

```

---

If you want, I can also add **a working `vite.config.js` + `.env` loader file** inside `src/config/env.js` so your project will automatically switch between development, staging, testing, and production without manual changes.  
That way the README + code will be 100% in sync.
```
