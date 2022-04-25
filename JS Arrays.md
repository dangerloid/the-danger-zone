---
aliases:
tags: study
---
[[JavaScript]]
# JS Arrays

Arrays allow you to store several pieces of data in one place.
They're surrounded by square brackets and every element within them is separated by a comma.

To declare an array:

```javascript
const myArray = ["Biscotto", 23];
```

## nesting

Arrays can be nested within each other.

```javascript
const myArray = [["Biscotto", 23], ["Budino", 14]];
```

## access array data with indexes

You can access data inside arrays through bracket notation.

```javascript
const myArray = [50, 60, 70];
var myData = myArray[0]; // output is 50
```

## modify array data with indexes

Array data can be modified unlike strings, even if the variable was declared with `const`.

```javascript
const myArray = [18, 64, 99];
myArray[0] = 45;
```

## access multi-dimensional arrays with indexes

You can use bracket notation to access multi-dimensional arrays (array of arrays, nesting).

```javascript
const myArray = [
	[1, 2, 3],
	[4, 5, 6],
	[7, 8, 9],
	[[10, 11, 12], 13, 14],
];
const myData = myArray[2][1];
```

`myArray[2][1]` is the second value in the third array, which equals to `8`.

## array manipulation

[[JS .push() function]]
[[JS .pop() function]]
[[JS .shift() function]]
[[JS .unshift() function]]

## shopping list (fCC exercise)

This is another example of [[JS Arrays#nesting|nesting]].

```js
const myList = [["cereal", 3], ["milk", 2], ["bananas", 3], ["juice", 2], ["eggs", 12]];
```