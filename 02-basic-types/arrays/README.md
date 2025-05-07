<img src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript Badge">

---


# Arrays in TypeScript

Arrays in TypeScript are used to store multiple values of the **same type**. You can explicitly specify the type of elements an array holds, which helps prevent runtime bugs and ensures consistency.

---

## 1. Basic Array Declaration

There are two ways to declare typed arrays:

### Using square brackets (`type[]`)

```ts
let scores: number[] = [95, 80, 70];
let names: string[] = ["Alice", "Bob", "Charlie"];
```

### Using the `Array<type>` syntax

```ts
let flags: Array<boolean> = [true, false, true];
```

Both approaches are functionally the same — choose whichever you find more readable.

---

## 2. Inline Example

```ts
let colors: string[] = ["red", "green", "blue"];

colors.push("yellow"); // ✅ Allowed
// colors.push(123);   // ❌ Error: Argument of type 'number' is not assignable to type 'string'

console.log(colors); // Output: ["red", "green", "blue", "yellow"]
```

---

## 3. Type Inference with Arrays

TypeScript can infer the array type based on the first values:

```ts
let ids = [1, 2, 3];      // inferred as number[]
let tags = ["ts", "js"];  // inferred as string[]
```

Once inferred, incorrect types will be rejected:

```ts
ids.push(4);    // ✅
ids.push("5");  // ❌ Error
```

---

## 4. Readonly Arrays

If you want an array that **cannot be changed**, use `readonly`:

```ts
const readonlyArr: readonly number[] = [1, 2, 3];

// readonlyArr.push(4);     // ❌ Error
// readonlyArr[0] = 99;     // ❌ Error
```

Useful for ensuring that some data remains immutable.

---

## 5. Array of Objects

```ts
let users: { name: string; age: number }[] = [
  { name: "Alice", age: 20 },
  { name: "Bob", age: 25 },
];

users.push({ name: "Charlie", age: 30 }); // ✅
```

---

## 6. Optional Elements (with `undefined`)

If some array slots may be `undefined`, use a union type:

```ts
let mixed: (number | undefined)[] = [1, 2, undefined, 4];
```

---

## Summary Table

| Syntax            | Description                         | Example                                 |                  |                 |
| ----------------- | ----------------------------------- | --------------------------------------- | ---------------- | --------------- |
| `type[]`          | Array of a specific type            | `let nums: number[] = [1, 2, 3];`       |                  |                 |
| `Array<type>`     | Generic array syntax                | `let flags: Array<boolean>`             |                  |                 |
| `readonly type[]` | Immutable array                     | `const arr: readonly string[] = [...]`  |                  |                 |
| \`type\[]         | undefined\[]\`                      | Optional or nullable elements           | \`let x: (string | undefined)\[]\` |
| `Array<object>`   | Array of structured object elements | `let users: { name: string }[] = [...]` |                  |                 |

---
![Static Badge](https://img.shields.io/badge/Aditya%20Kumar-black?style=for-the-badge&logo=atlasos&logoColor=%23ffffff)