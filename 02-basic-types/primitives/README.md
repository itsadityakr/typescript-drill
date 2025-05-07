<img src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript Badge">

---


# Primitives in TypeScript

In TypeScript, primitives are basic types that represent simple values, such as numbers, strings, booleans, and more. These types are the building blocks for all other types and are fundamental for ensuring type safety in your programs.

## 1. **Number**

The `number` type in TypeScript is used to represent both integer and floating-point values. It is one of the most commonly used primitive types.

### Example:

```ts
let age: number = 25;
let price: number = 19.99;

console.log(age);   // Output: 25
console.log(price); // Output: 19.99
```

### Special Cases:

* `Infinity`, `-Infinity`, and `NaN` are valid `number` values in TypeScript.

```ts
let inf: number = Infinity;   // Valid number
let nan: number = NaN;        // Valid number
```

## 2. **String**

The `string` type is used for representing textual data, such as words, sentences, or any sequence of characters.

### Example:

```ts
let firstName: string = "John";
let greeting: string = "Hello, " + firstName;

console.log(greeting); // Output: "Hello, John"
```

### Template Literals:

You can use template literals to easily include variables within strings:

```ts
let age: number = 25;
let message: string = `I am ${age} years old`;

console.log(message); // Output: "I am 25 years old"
```

## 3. **Boolean**

The `boolean` type represents a value that is either `true` or `false`. It is commonly used for conditional logic, like controlling loops or making decisions.

### Example:

```ts
let isActive: boolean = true;
let isComplete: boolean = false;

console.log(isActive);   // Output: true
console.log(isComplete); // Output: false
```

## 4. **Null**

The `null` type represents the intentional absence of any value or object. It is commonly used to indicate that a variable is explicitly set to no value.

### Example:

```ts
let user: string | null = null;

console.log(user); // Output: null
```

## 5. **Undefined**

The `undefined` type represents a variable that has not been assigned a value. In TypeScript, if you declare a variable but do not initialize it, its value will be `undefined`.

### Example:

```ts
let score: number;
console.log(score); // Output: undefined
```

## 6. **Symbol**

The `symbol` type is a newer primitive type introduced in ES6. Symbols are unique and immutable values that can be used as object keys or for other unique identifiers.

### Example:

```ts
let sym1: symbol = Symbol("unique");
let sym2: symbol = Symbol("unique");

console.log(sym1 === sym2); // Output: false (symbols are unique)
```

## 7. **BigInt**

The `BigInt` type is used to represent arbitrarily large integers. It was introduced in ES2020 and allows you to work with numbers beyond the safe integer limit of `number`.

### Example:

```ts
let bigNumber: BigInt = 1234567890123456789012345678901234567890n;

console.log(bigNumber); // Output: 1234567890123456789012345678901234567890n
```

## 8. **Primitive Type Inference**

TypeScript can infer the primitive type based on the initial value, so you don’t always need to explicitly define the type.

### Example:

```ts
let age = 30;  // inferred as 'number'
let isActive = true;  // inferred as 'boolean'
let name = "Alice";  // inferred as 'string'
```

## 9. **Comparing Primitives**

When comparing primitive types like numbers, strings, and booleans, TypeScript uses value-based comparison. This means that two variables of the same type with the same value are considered equal.

### Example:

```ts
let a = 10;
let b = 10;

console.log(a === b); // Output: true
```

---

### Summary Table

| **Type**    | **Description**                                 | **Example**                                               |
| ----------- | ----------------------------------------------- | --------------------------------------------------------- |
| `number`    | Represents numeric values (integers and floats) | `let age: number = 25;`                                   |
| `string`    | Represents textual data                         | `let name: string = "Alice";`                             |
| `boolean`   | Represents true or false values                 | `let isActive: boolean = true;`                           |
| `null`      | Represents the intentional absence of any value | `let user: null = null;`                                  |
| `undefined` | Represents a variable with no assigned value    | `let score: number;`                                      |
| `symbol`    | Represents unique identifiers                   | `let sym = Symbol("unique");`                             |
| `BigInt`    | Represents large integers                       | `let bigNum = 1234567890123456789012345678901234567890n;` |


---
![Static Badge](https://img.shields.io/badge/Aditya%20Kumar-black?style=for-the-badge&logo=atlasos&logoColor=%23ffffff)