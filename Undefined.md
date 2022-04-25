---
aliases:
tags: study
---
[[JS Data Types]]
# Undefined

Undefined is something that hasn't been defined.

An example might be:

```javascript
var myVar;
```

The console output for this variable will be `undefined`.

## `undefined` in functions

A function can include the `return` statement but it does not have to. Calling a function that doesn't have a `return` statement, returns undefined.

```js
let sum = 0;

function addThree() {
	sum = sum + 3;
}

function addFive() {
	sum = sum + 5;
}

addThree();
addFive();
```

