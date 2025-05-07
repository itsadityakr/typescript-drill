<img src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript Badge">

---


# Type Inference in TypeScript

TypeScript's type inference system automatically determines the type of a variable based on its initial value or usage. This feature helps you write concise code without explicitly annotating types for every variable. Type inference ensures that TypeScript understands the types of your variables and provides type checking accordingly.

## 1. **Basic Type Inference**

TypeScript infers the type of a variable based on its initial value. If you initialize a variable with a specific type, TypeScript automatically determines its type.

### Example:

```ts
let message = "Hello, TypeScript!"; // inferred as 'string'

console.log(message);  // Output: "Hello, TypeScript!"
```

Here, TypeScript infers the type of `message` as `string` because it is initialized with a string value.

### Incorrect Type Assignment:

```ts
let message = "Hello, TypeScript!"; // inferred as 'string'
message = 42;  // ❌ Error: Type 'number' is not assignable to type 'string'
```

Since `message` is inferred as a `string`, assigning a `number` value results in a type error.

## 2. **Inferred Types for Arrays**

TypeScript can infer the type of arrays based on their elements. If you initialize an array with a specific type, TypeScript infers the type for all elements in the array.

### Example:

```ts
let numbers = [1, 2, 3];  // inferred as 'number[]'

console.log(numbers);  // Output: [1, 2, 3]
```

Here, TypeScript infers the type of `numbers` as `number[]` because the array contains only numbers.

### Incorrect Type Assignment:

```ts
let numbers = [1, 2, 3];  // inferred as 'number[]'
numbers.push("four");  // ❌ Error: Argument of type 'string' is not assignable to parameter of type 'number'
```

You cannot push a `string` to an array inferred as `number[]`.

## 3. **Inferred Types for Objects**

When initializing objects, TypeScript infers the type of the object based on its properties and their types.

### Example:

```ts
let person = {
  name: "Alice",
  age: 30
};  // inferred as { name: string; age: number; }

console.log(person);  // Output: { name: "Alice", age: 30 }
```

Here, TypeScript infers that `person` has a `name` of type `string` and an `age` of type `number`.

### Incorrect Type Assignment:

```ts
let person = {
  name: "Alice",
  age: 30
};  // inferred as { name: string; age: number; }

person.age = "thirty";  // ❌ Error: Type 'string' is not assignable to type 'number'
```

If you try to assign a `string` to the `age` property, TypeScript will throw an error because `age` is inferred as a `number`.

## 4. **Type Inference with Functions**

TypeScript can infer the return type of a function based on its return statements. If the function has an explicit return value, TypeScript will automatically deduce the return type.

### Example:

```ts
function add(x: number, y: number) {
  return x + y;  // inferred return type is 'number'
}

console.log(add(5, 3));  // Output: 8
```

In this example, TypeScript infers the return type of `add` as `number` because the function returns a sum of two numbers.

### Return Type Inference with Type Annotations:

```ts
function greet(name: string): string {
  return "Hello, " + name;  // return type explicitly annotated as 'string'
}

console.log(greet("Alice"));  // Output: "Hello, Alice"
```

Here, the return type is explicitly annotated as `string`.

## 5. **Inferred `any` Type**

If TypeScript cannot infer the type of a variable due to insufficient information, it will assign the `any` type to that variable. This allows for flexibility, but should be avoided where possible, as it disables type checking for that variable.

### Example:

```ts
let data;  // inferred as 'any'

data = 42;     // no error
data = "text"; // no error
```

### Avoiding `any`:

To prevent variables from being inferred as `any`, always initialize them with a specific type.

```ts
let data: number = 42;  // explicitly declared as 'number'
```

## 6. **Type Inference in Complex Scenarios**

TypeScript can also infer types in more complex scenarios, such as when using generics, or when an array or object has mixed types. However, in these cases, it’s usually recommended to provide explicit types for clarity and safety.

### Example with Mixed Types:

```ts
let data = [1, "hello", true];  // inferred as (string | number | boolean)[]
```

Here, TypeScript infers that `data` is an array containing `string`, `number`, and `boolean` types.

### Example with Generics:

```ts
function identity<T>(arg: T): T {
  return arg;
}

let result = identity(42);  // inferred as 'number'
let text = identity("hello");  // inferred as 'string'
```

## 7. **Using `const` for Inference**

When you use `const` to declare variables, TypeScript infers a **literal type** for the variable. This means that `const` variables are considered to have the exact value they are assigned, rather than their general type.

### Example:

```ts
const pi = 3.14;  // inferred as 3.14 (literal type, not just 'number')
const greeting = "Hello";  // inferred as "Hello" (literal type)
```

Here, `pi` is inferred as the literal type `3.14`, and `greeting` is inferred as the literal type `"Hello"`.

---

### Summary Table

| **Feature**                   | **Description**                                                                 | **Example**                                            |
| ----------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------ |
| **Basic Inference**           | TypeScript infers type based on the initial value                               | `let message = "Hello";`                               |
| **Arrays**                    | TypeScript infers the array type based on the elements                          | `let numbers = [1, 2, 3];`                             |
| **Objects**                   | TypeScript infers object types based on the properties                          | `let person = { name: "Alice", age: 30 };`             |
| **Functions**                 | TypeScript infers the return type based on the return value                     | `function add(x: number, y: number) { return x + y; }` |
| **`any` Type**                | TypeScript uses `any` when it cannot infer a type, which disables type checking | `let data;`                                            |
| **`const` and Literal Types** | TypeScript infers literal types for `const` variables                           | `const pi = 3.14;`                                     |
| **Generics and Mixed Types**  | TypeScript can infer types with generics or mixed-type arrays/objects           | `let data = [1, "hello", true];`                       |


---
![Static Badge](https://img.shields.io/badge/Aditya%20Kumar-black?style=for-the-badge&logo=atlasos&logoColor=%23ffffff)