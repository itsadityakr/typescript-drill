<img src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript Badge">

---

# Installing TypeScript and Common Commands

To start using TypeScript, you need Node.js and the TypeScript compiler (`tsc`) installed on your machine. This section walks you through the entire setup, verifies installations, and explains the most common TypeScript commands.

---

## Step 1: Check if Node.js is installed

TypeScript runs on Node.js, so make sure Node is available.

```bash
node --version
```

If it outputs a version like `v18.17.0`, you're good to go. If not, download and install Node.js from [https://nodejs.org](https://nodejs.org).

---

## Step 2: Install TypeScript globally

You can install TypeScript globally using any package manager like `npm`, `pnpm`, or `yarn`.

### Using npm:

```bash
npm install -g typescript
```

### Using pnpm:

```bash
pnpm add -g typescript
```

This installs the TypeScript compiler and makes the `tsc` command available.

---

## Step 3: Check TypeScript installation

After installation, verify it using:

```bash
tsc --version
```

You should see something like `Version 5.x.x`.

---

## Step 4: Initialize a TypeScript project

There are two common ways to initialize TypeScript in a project:

### Option 1: Global `tsc` command

```bash
tsc --init
```

This creates a `tsconfig.json` file in your project directory, which is used to configure the TypeScript compiler settings.

### Option 2: Using `npx` (if not installed globally)

```bash
npx tsc --init
```

This works even if `tsc` isn't installed globally. `npx` downloads and runs it just-in-time.

---

## Step 5: Understanding `tsconfig.json`

The `tsconfig.json` file tells TypeScript how to compile your code. It includes settings like:

```json
{
  "compilerOptions": {
    "target": "es6",
    "module": "commonjs",
    "outDir": "./dist",
    "rootDir": "./src",
    "strict": true
  }
}
```

You can customize it based on your project structure and needs.

---

## Step 6: Compiling TypeScript Files

To compile a TypeScript file (e.g., `app.ts`) to JavaScript:

```bash
tsc app.ts
```

This will create `app.js` in the same directory.

If you have multiple files and a `tsconfig.json`:

```bash
tsc
```

This compiles the entire project according to your configuration.

---

## Step 7: Watch for changes

For continuous development, use:

```bash
tsc --watch
```

This watches your TypeScript files and automatically re-compiles them when you make changes.

---

## Summary of Useful Commands

| Command               | Purpose                                              |
| --------------------- | ---------------------------------------------------- |
| `node --version`      | Check if Node.js is installed                        |
| `tsc --version`       | Check installed TypeScript version                   |
| `tsc --init`          | Create a `tsconfig.json` file                        |
| `npx tsc --init`      | Initialize TypeScript project without global install |
| `npm i typescript -g` | Install TypeScript globally                          |
| `tsc app.ts`          | Compile a single TypeScript file                     |
| `tsc`                 | Compile all files using `tsconfig.json`              |
| `tsc --watch`         | Automatically recompile on file changes              |

---
![Static Badge](https://img.shields.io/badge/Aditya%20Kumar-black?style=for-the-badge&logo=atlasos&logoColor=%23ffffff)