Here's a clean and beginner-friendly **GitHub README-style Markdown** section for **"Installing TypeScript"**, continuing from the previous format:

---

# Installing TypeScript

To start using TypeScript, you need to install it on your system using **Node.js** and **npm (Node Package Manager)**.

---

## 1. Prerequisites

Before installing TypeScript, make sure you have **Node.js** installed.

### Check if Node.js is installed:

```bash
node -v
npm -v
```

If not installed, download from: [https://nodejs.org](https://nodejs.org)

---

## 2. Install TypeScript Globally

This allows you to use the `tsc` (TypeScript Compiler) command from anywhere.

```bash
npm install -g typescript
```

### Check if installed:

```bash
tsc -v
```

> ✅ Output Example: `Version 5.3.2` (your version may differ)

---

## 3. Create a TypeScript File

You can now create a `.ts` file and start coding.

```ts
// hello.ts
let message: string = "Hello, TypeScript!";
console.log(message);
```

---

## 4. Compile TypeScript to JavaScript

Use the `tsc` command to convert `.ts` to `.js`.

```bash
tsc hello.ts
```

This creates a new `hello.js` file:

```js
// hello.js
var message = "Hello, TypeScript!";
console.log(message);
```

Run it with Node.js:

```bash
node hello.js
```

> ✅ Output: `Hello, TypeScript!`

---

## 5. Summary

* ✅ Install Node.js and npm
* ✅ Install TypeScript globally with `npm install -g typescript`
* ✅ Compile `.ts` files using `tsc`
* ✅ Run the output `.js` files with `node`

---

Ready to move on to **setting up a project folder** or **basic types** next?
