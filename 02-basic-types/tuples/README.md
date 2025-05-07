<img src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript Badge">

---


# Tuples in TypeScript

In TypeScript, tuples are a special type of array where the elements can be of different types and are fixed in length. Tuples provide a way to store data in a specific sequence, where each element can have a different type. This allows for more precise type checking when dealing with heterogeneous data collections.

## 1. **Basic Tuple Declaration**

Tuples are defined using square brackets, where each element’s type is specified in order.

### Example:

```ts
let person: [string, number] = ["Alice", 30];

console.log(person);   // Output: ["Alice", 30]
```

In this example, `person` is a tuple that contains a `string` and a `number`, in that order.

### Tuple with Multiple Types:

```ts
let product: [string, number, boolean] = ["Laptop", 999.99, true];

console.log(product);  // Output: ["Laptop", 999.99, true]
```

## 2. **Accessing Tuple Elements**

You can access the elements of a tuple by their index, just like with arrays.

### Example:

```ts
let person: [string, number] = ["Alice", 30];

console.log(person[0]);   // Output: Alice
console.log(person[1]);   // Output: 30
```

## 3. **Tuple with Optional Elements**

Tuples can also have optional elements, which are indicated by appending `?` to the type of the element. The optional elements can either be `undefined` or a specific value.

### Example:

```ts
let person: [string, number, string?] = ["Alice", 30];

console.log(person);  // Output: ["Alice", 30]
```

In this example, the third element is optional and may be omitted.

### Optional Element with a Value:

```ts
let person: [string, number, string?] = ["Alice", 30, "Engineer"];

console.log(person);  // Output: ["Alice", 30, "Engineer"]
```

## 4. **Tuple with Rest Elements**

TypeScript allows you to define a tuple with rest elements using the `...` syntax. This means that the tuple can have a variable number of elements of the same type after the specified elements.

### Example:

```ts
let colors: [string, ...number[]] = ["red", 255, 0, 0];

console.log(colors);  // Output: ["red", 255, 0, 0]
```

In this case, the first element must be a `string`, and any number of `number` elements can follow.

## 5. **Tuple with Mixed Types**

Tuples can hold elements of different types in specific positions, allowing you to represent structured data in a single array-like structure.

### Example:

```ts
let user: [string, number, boolean] = ["Alice", 25, true];

console.log(user);  // Output: ["Alice", 25, true]
```

## 6. **Type Inference in Tuples**

Just like arrays, TypeScript can infer the type of a tuple based on its initial values.

### Example:

```ts
let person = ["Alice", 30];  // Inferred as [string, number]

console.log(person);  // Output: ["Alice", 30]
```

### Incorrect Tuple Assignment:

```ts
let person: [string, number] = ["Alice", 30];
person = [30, "Alice"];  // ❌ Error: Type 'number' is not assignable to type 'string'.
```

The tuple structure is strict about the order of the types, so attempting to switch the positions will result in a type error.

## 7. **Destructuring Tuples**

You can use destructuring to unpack tuple elements into individual variables.

### Example:

```ts
let person: [string, number] = ["Alice", 30];

let [name, age] = person;

console.log(name);  // Output: Alice
console.log(age);   // Output: 30
```

## 8. **Named Tuples (with Labels)**

In TypeScript, you can provide labels for tuple elements, which can make your code more readable and help with auto-completion in IDEs.

### Example:

```ts
let person: [name: string, age: number] = ["Alice", 30];

console.log(person[0]);  // Output: Alice (Accessing by name 'name')
console.log(person[1]);  // Output: 30 (Accessing by name 'age')
```

## 9. **Readonly Tuples**

To make a tuple immutable (read-only), use `readonly` before the tuple definition. This prevents any modification of the tuple's elements after initialization.

### Example:

```ts
const person: readonly [string, number] = ["Alice", 30];

// person[0] = "Bob";  // ❌ Error: Index signature in type 'readonly [string, number]' only permits reading.
```

---

### Summary Table

| **Syntax**                     | **Description**                                 | **Example**                                                |
| ------------------------------ | ----------------------------------------------- | ---------------------------------------------------------- |
| `[type1, type2]`               | Basic tuple with specific types in order        | `let person: [string, number] = ["Alice", 30];`            |
| `[type1, type2, type3?]`       | Tuple with an optional element                  | `let person: [string, number, string?] = ["Alice", 30];`   |
| `[firstElement, ...rest]`      | Tuple with rest elements of the same type       | `let colors: [string, ...number[]] = ["red", 255, 0, 0];`  |
| `let tuple = [value1, value2]` | TypeScript infers types based on initial values | `let person = ["Alice", 30];`                              |
| `readonly [type1, type2]`      | Immutable tuple, prevents modification          | `const person: readonly [string, number] = ["Alice", 30];` |

---

![Static Badge](https://img.shields.io/badge/Aditya%20Kumar-black?style=for-the-badge&logo=atlasos&logoColor=%23ffffff)