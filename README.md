# **Fastify TypeScript Starter Project**

A starter template for building robust server-side applications using **Fastify** with **TypeScript**. This repository is designed for scalability, readability, and best practices. Includes integration with **Prettier**, **ESLint**, and **Typedoc** for a well-maintained codebase.

---

## **Features**

- 🚀 **Fastify**: A high-performance web framework.
- 🛠 **TypeScript**: Type-safe development with strict configurations.
- 🎨 **Prettier**: Automatic code formatting for a consistent style.
- 🔍 **ESLint**: Linting for cleaner and error-free code.
- 📚 **Typedoc**: Generate documentation for your code.
- 🗂 **Path Aliases**: Simplified imports using `@src`, `@routes`, `@services`, etc.
- 🔄 Development and production-specific TypeScript configurations.

---

## **Project Setup**

### **1. Clone the Repository**
```bash
git clone https://github.com/bkapilsharmadev/fastify-typescript-sample.git
cd fastify-typescript-sample
```

### **2. InstallDependencies**
```bash
npm install
```

### **3. Run the project**
- For Development
```bash
npm run dev
```
- For Production
```bash
npm run build && npm start
```

### **4. Scripts**
| Script         | Command                                                       | Purpose                                                                                                 |
|----------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| `clean`        | `rimraf dist`                                                 | Deletes the `dist` directory to ensure a clean build environment.                                       |
| `build:dev`    | `tsc -p tsconfig.dev.json && tsc-alias`                       | Compiles TypeScript in development mode using `tsconfig.dev.json` and resolves path aliases.            |
| `build:prod`   | `tsc -p tsconfig.prod.json && tsc-alias`                      | Compiles TypeScript in production mode using `tsconfig.prod.json` and resolves path aliases.            |
| `start`        | `npm run build:prod && node dist/index.js`                    | Builds the project in production mode and starts the application.                                       |
| `dev`          | `npm run lint && npm run format && tsc-watch -p tsconfig.dev.json --onSuccess \"npm run start:alias\"`             | Lints, formats, and starts the application in watch mode for development.                               |
| `start:alias`  | `tsc-alias -p tsconfig.dev.json && nodemon dist/index.js`     | Resolves path aliases and starts the server with `nodemon` for live reloads.                            |
| `lint`         | `eslint src`                                                  | Lints the codebase using ESLint to ensure code quality and style consistency.                           |
| `format`       | `prettier --write src/**/*.ts`                                | Formats the codebase using Prettier to maintain a consistent style.                                     |
| `prepare`      | `husky`                                                       | Runs Husky setup to enable Git hooks for tasks like pre-commit linting or formatting.                   |
