<img src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript Badge">

---

# Recommended VS Code Extensions for TypeScript Development

To make your TypeScript development smoother, faster, and more consistent, these Visual Studio Code extensions are highly recommended. They help with linting, formatting, live preview, better error messages, and staying updated with the latest TypeScript features.

---

## 1. ESLint

**Lint your code to follow best practices and catch errors.**

* 📦 Extension: [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
* Adds real-time linting for JavaScript and TypeScript using your ESLint configuration.

### Usage Example:

```ts
const a = 5
```

Without a semicolon, ESLint will underline the issue if your rules require it.

---

## 2. Prettier - Code formatter

**Automatically formats code based on style rules.**

* 📦 Extension: [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

### Example:

Before formatting:

```ts
const name="Aditya"
```

After formatting:

```ts
const name = "Aditya";
```

---

## 3. Prettier ESLint

**Combines Prettier’s formatting with ESLint’s rules for a cleaner and consistent codebase.**

* 📦 Extension: [Prettier ESLint](https://marketplace.visualstudio.com/items?itemName=rvest.vs-code-prettier-eslint)

### Use Case:

This extension ensures that code is not only pretty but also follows your linting rules.

---

## 4. Live Server

**Launch a development local server with live reload feature.**

* 📦 Extension: [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)

### Usage:

Right-click on an `index.html` file and select **"Open with Live Server"**. Any changes you make will automatically refresh the browser.

---

## 5. JavaScript and TypeScript Nightly

**Stay updated with the latest TypeScript features before they are officially released.**

* 📦 Extension: [JavaScript and TypeScript Nightly](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-typescript-next)

> Ideal for developers who want to experiment with new TypeScript features as they are developed.

---

## 6. Pretty TypeScript Errors

**Improves the formatting of TypeScript error messages for readability.**

* 📦 Extension: [Pretty TypeScript Errors](https://marketplace.visualstudio.com/items?itemName=yoavbls.pretty-ts-errors)

### Example:

Instead of a long unreadable error message, you'll get a clean and focused message like:

```
Cannot assign a string to a number.
Type 'string' is not assignable to type 'number'.
```

This is especially helpful when working with large files or nested types.

---

## Summary Table

| Extension Name           | Purpose                              | Link                                                                                         |
| ------------------------ | ------------------------------------ | -------------------------------------------------------------------------------------------- |
| ESLint                   | Lint JavaScript/TypeScript           | [View](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)           |
| Prettier                 | Format code consistently             | [View](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)           |
| Prettier ESLint          | Combine Prettier with ESLint rules   | [View](https://marketplace.visualstudio.com/items?itemName=rvest.vs-code-prettier-eslint)    |
| Live Server              | Live reload local development server | [View](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)            |
| JS/TS Nightly            | Access nightly builds of TypeScript  | [View](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-typescript-next) |
| Pretty TypeScript Errors | Makes TS errors readable             | [View](https://marketplace.visualstudio.com/items?itemName=yoavbls.pretty-ts-errors)         |


---
![Static Badge](https://img.shields.io/badge/Aditya%20Kumar-black?style=for-the-badge&logo=atlasos&logoColor=%23ffffff)