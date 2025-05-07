<img src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript Badge">

---

# Setting Up the TypeScript Environment

Before writing real TypeScript projects, it’s best to set up a dedicated environment with configuration, organized code, and automatic compilation.

---

## 1. Create a Project Folder

```bash
mkdir my-typescript-project
cd my-typescript-project
```

---

## 2. Initialize the Project with `npm`

This creates a `package.json` file to manage your project dependencies.

```bash
npm init -y
```

> ✅ Output: A `package.json` file is generated.

---

## 3. Install TypeScript Locally

Install TypeScript only for this project (not globally).

```bash
npm install typescript --save-dev
```

---

## 4. Create a TypeScript Configuration File

Generate a `tsconfig.json` file which controls how TypeScript compiles your code.

```bash
npx tsc --init
```

> ✅ Output: A `tsconfig.json` file is created with default settings.

---

## 5. Create Source and Output Folders

Organize your code in `src` and output JavaScript in `dist`.

```bash
mkdir src
mkdir dist
```

Edit your `tsconfig.json` to set compiler options:

```json
{
  "compilerOptions": {
    "target": "es6",
    "outDir": "./dist",
    "rootDir": "./src",
    "strict": true
  }
}
```

---

## 6. Write Your First File

Create a file inside `src/hello.ts`:

```ts
// src/hello.ts
const greet = (name: string): string => {
  return `Hello, ${name}`;
};

console.log(greet("TypeScript"));
```

---

## 7. Compile the Project

```bash
npx tsc
```

> ✅ Output: Compiled `hello.js` appears inside the `dist` folder.

---

## 8. Run the Output File

```bash
node dist/hello.js
```

> ✅ Output: `Hello, TypeScript`

---

## Summary

* Use `npm` to manage your project.
* Organize code with `src/` and `dist/`.
* Use `tsconfig.json` to control compilation.
* Use `npx tsc` to compile TypeScript to JavaScript.

---
![Static Badge](https://img.shields.io/badge/Aditya%20Kumar-black?style=for-the-badge&logo=atlasos&logoColor=%23ffffff)