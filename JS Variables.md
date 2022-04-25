---
aliases: [Variable, var, let, const]
tags: study
---
[[JavaScript]]
# Variables

Variables can store data dynamically (not exclusive to JavaScript. Most if not all programming languages have them).

The value of a variable can be any of the eight [[JS Data Types]], but it's common to set it to a [[String]].

## assigning a variable

You can set a variable with the keyword `var`.

```javascript
var myName = "Chris";
```

Since `myName` is a variable, it can be changed somewhere else in the document.

```javascript
myName = 9;
```

Since the variable has been updated, the value of `myName` is not `"Chris"` anymore, but `9`.

## declaring a variable

There are three keywords to declare a variable:
- `var`
- `let`
- `const`

### `var`
It was the only way to declare a variable until a few years ago.
A variable set with `var` will be used throughout the whole program, it has global scope.

### `let`
A variable set with `let` will only be used within the local scope (i.e. a function).

### `const`
`const` is a variable that can't be changed (read-only). If you change it you'll get an error message when running or debugging your code. You should always declare variables you don't want to reassign with `const`.

Example: 

```javascript
const FAV_PET = "Cats";
FAV_PET = "Dogs";
```

This will output an error.

Best practice recommends writing the constant's name in uppercase, with each word separated by an underscore.