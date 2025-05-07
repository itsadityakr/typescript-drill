<img src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript Badge">

---

# `any`, `unknown`, and `void` in TypeScript

These are three special types in TypeScript that help you deal with uncertain or absent values. While powerful, they must be used with caution to keep your code type-safe.

---

## 1. `any` Type

The `any` type **disables all type checking**. Use it only when you want to opt-out of TypeScript's safety.

### Example:

```ts
let data: any = 10;
data = "hello";
data = true;
```

* `any` can hold any type of value.
* TypeScript won't check or enforce anything.
* Avoid using `any` unless necessary.

### Why avoid `any`?

```ts
let input: any = "text";
console.log(input.toUpperCase()); // ✅ Works
input = 5;
console.log(input.toUpperCase()); // ❌ Runtime error, not caught at compile time
```

---

## 2. `unknown` Type

The `unknown` type is like `any`, but **TypeScript forces you to check the type** before using it.

### Example:

```ts
let value: unknown = "TypeScript";

if (typeof value === "string") {
  console.log(value.toUpperCase()); // ✅ Safe
}
```

* You can’t directly perform operations on an `unknown` value.
* Forces you to narrow the type using `typeof`, `instanceof`, or type guards.

### Use Case:

Use `unknown` when receiving data from outside sources (e.g. APIs, user input) and you want to enforce type checking later.

---

## 3. `void` Type

The `void` type is used for **functions that don’t return anything**.

### Example:

```ts
function logMessage(message: string): void {
  console.log(message);
}
```

* The function does something (like logging) but doesn't return a value.
* Trying to return a value will show a compile-time error:

```ts
function errorExample(): void {
  return "text"; // ❌ Error: Type '"text"' is not assignable to type 'void'.
}
```

---

## Summary Table

| Type      | Description                                | Use Case                                  | Safe to Use |
| --------- | ------------------------------------------ | ----------------------------------------- | ----------- |
| `any`     | Turns off type checking                    | Quick prototyping, external JS            | ❌ No        |
| `unknown` | Like `any`, but must check type before use | Handling uncertain input or external data | ✅ Yes       |
| `void`    | No return value                            | Function that returns nothing             | ✅ Yes       |

---

## Quick Comparison

```ts
let a: any = 123;
let b: unknown = "TS";

// `any` lets you do anything
console.log(a.toFixed());   // ✅ OK
a = "hello";
console.log(a.toUpperCase()); // ✅ OK, but unsafe

// `unknown` must be checked
if (typeof b === "string") {
  console.log(b.toUpperCase()); // ✅ OK
}
```

---
![Static Badge](https://img.shields.io/badge/Aditya%20Kumar-black?style=for-the-badge&logo=atlasos&logoColor=%23ffffff)