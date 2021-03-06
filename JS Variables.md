---
aliases: [Variable, var, let, const]
tags: study
---
[[JS Basics + ES6 Features]]
# Variables

Variables can store data dynamically (not exclusive to JavaScript. Most if not all programming languages have them).

The value of a variable can be any of the eight [[JS Data Types]], but it's common to set it to a [[JS String]].

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

## compare scopes of the `var` and `let` keywords
When you declare a variable with the `var` keyword, it is declared globally, or locally if inside a function.

The `let` keyword behaves similarly, but has some differences.
When you declare a variable with `let` inside a block, statement or expression, its scope is limited to that block, statement or expression.

## mutate an array declared with `const`
Some developers prefer to assign all their variables using `const` by default, unless they know they're gonna reassign the value.

It's important to know that objects assigned to a variable using `const` are still mutable ([[JS Object|we've seen that]]). Using `const` only prevents reassignment of the variable identifier.