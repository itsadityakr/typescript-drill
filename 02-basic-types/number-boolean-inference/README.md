<img src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript Badge">

---

# Number and Boolean Inference in TypeScript

In TypeScript, type inference automatically determines the type of a variable based on its initial value. This means that TypeScript can infer whether a variable should be a `number` or a `boolean` without you needing to explicitly define the type. Understanding how TypeScript infers these types helps write more concise code.

## 1. **Number Inference**

TypeScript can infer the type `number` for a variable if it is initialized with a numeric value. This makes it unnecessary to explicitly declare the type in many cases.

### Example:

```ts
let age = 30;   // inferred as 'number'

console.log(age);  // Output: 30
```

Since `age` is assigned a numeric value, TypeScript automatically infers its type as `number`. You don’t need to write `let age: number`.

### Incorrect Type Assignment:

```ts
let age = 30;   // inferred as 'number'
age = "hello";   // ❌ Error: Type 'string' is not assignable to type 'number'
```

Here, trying to assign a `string` to a variable that was inferred to be a `number` results in a type error.

## 2. **Boolean Inference**

Similarly, TypeScript infers the type `boolean` when a variable is initialized with a `true` or `false` value.

### Example:

```ts
let isActive = true;   // inferred as 'boolean'

console.log(isActive);  // Output: true
```

In this case, TypeScript infers that `isActive` is of type `boolean` because it is assigned a `true` value.

### Incorrect Type Assignment:

```ts
let isActive = true;   // inferred as 'boolean'
isActive = 5;          // ❌ Error: Type 'number' is not assignable to type 'boolean'
```

If we try to assign a `number` to a variable inferred as `boolean`, TypeScript throws an error.

## 3. **Type Inference with `let` vs. `const`**

* When using `let`, TypeScript can infer a variable's type but still allow it to be reassigned to a compatible type.
* When using `const`, TypeScript infers both the type and makes it immutable, preventing reassignment.

### Example with `let`:

```ts
let count = 100;   // inferred as 'number'
count = 200;       // ✅ Allowed, count is mutable
```

### Example with `const`:

```ts
const isLoggedIn = false;   // inferred as 'boolean'
// isLoggedIn = true;         // ❌ Error: Cannot assign to 'isLoggedIn' because it is a constant.
```

## 4. **Explicit Type Annotations vs. Inference**

While TypeScript infers types in many cases, you can still explicitly declare types when needed for clarity or to avoid unexpected behavior.

### Example of Explicit Type Annotations:

```ts
let age: number = 25;    // explicitly defined as 'number'
let isActive: boolean = false;   // explicitly defined as 'boolean'
```

This can be helpful when you want to ensure the variable's type is strictly controlled or when it's not obvious what type the variable will have.

---

### Summary Table

| **Syntax**                         | **Description**                                            | **Example**                 |
| ---------------------------------- | ---------------------------------------------------------- | --------------------------- |
| `let variable = 10`                | TypeScript infers a `number` from initial value            | `let age = 30;`             |
| `let variable = true`              | TypeScript infers a `boolean` from initial value           | `let isActive = true;`      |
| `let` vs. `const`                  | `let` allows reassignment, `const` prevents it             | `const isLoggedIn = false;` |
| Type Inference vs. Type Annotation | TypeScript can infer types, or you can explicitly annotate | `let age: number = 25;`     |

---
![Static Badge](https://img.shields.io/badge/Aditya%20Kumar-black?style=for-the-badge&logo=atlasos&logoColor=%23ffffff)