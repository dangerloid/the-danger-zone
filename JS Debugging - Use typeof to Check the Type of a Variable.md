---
aliases:
tags: study
---
[[JS Debugging]]
# JS Debugging - Use typeof to Check the Type of a Variable
You can use `typeof` to check the data structure, or type, of a variable. This is useful in debugging when working with multiple data types.
Type errors can lurk in calculations or function calls. Be careful especially when you're accessing and working with external data in the form of a JSON object.

Examples of `typeof`:

```js
console.log(typeof ""); // returns string
console.log(typeof 0); // returns number
console.log(typeof []); // returns object
console.log(typeof {}); // returns object
```

JavaScript recognizes seven primitive data types: `boolean`, `null`, `undefined`, `number`, `symbol` and `bigInt`, and one type for mutable items, `object`. Arrays are considered objects.

Exercise: add two `console.log()` statements to check the `typeof` each of the two variables.