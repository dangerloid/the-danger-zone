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

## use the spread operator to evaluate arrays in-place
ES6 introduced the spread operator, which allows for expansion of arrays and other expressions in places where multiple parameters or elements are expected.

This is ES5 code. It uses `apply()` to compute the maximum value in an array:

```js
var arr = [6, 89, 3, 45];
var maximus = Math.max.apply(null, arr); // value is 89
```

We had to use `Math.max.apply(null, arr)` because `Math.max(arr)` returns `NaN`. `Math.max()` expects comma-separated arguments, but not an array. The spread operator makes this syntax better to read and maintain.

```js
const arr = [6, 89, 3, 45];
const maximus = Math.max(...arr);
```

`...arr` returns an unpacked array.
The spread operator works in-place, like function arguments.

Exercise: copy all contents of `arr1` into another array using the spread operator.

```js
const arr1 = ['JAN', 'FEB', 'MAR', 'APR', 'MAY'];
let arr2;

arr2 = [...arr1];
```

## use destructuring assignment to assign variables from arrays
ES6 can let you destructure arrays as well.

The difference between the spread operator and array destructuring is that the spread operator unpacks all the content of an array into a comma-separated list and you cannot pick or choose which element you want to assign to variables.

Enter array destructuring:

```js
const [a, b] = [1, 2, 3, 4, 5, 6];
console.log(a, b);
```

The console will display the values of `a` and `b` as `1, 2`.

The variable `a` is assigned the first value of the array and `b` is assigned the second value. We can access the value at any index of the array with destructuring by using commas to reach the desired index:

```js
const [a, b,,, c] = [1, 2, 3, 4, 5, 6];
console.log(a, b, c);
```
The console will display the values of `a`, `b` and `c` as `1, 2, 5`.

Exercise: use destructuring assignment to swap the values of `a` and `b` so that `a` receives the value stored in `b` and viceversa.

```js
let a = 8, b = 6;
[a, b] = [b, a];
```

## use destructuring assignment with the rest parameter to reassign array elements
In some situations involving array destructuring, we might want to collect the rest of the elements into a separate array, like this:

```js
const [a, b, ...arr] = [1, 2, 3, 4, 5, 7];
```

The console would display the values `1, 2` and `[3, 4, 5, 7]`.

Variables `a` and `b` take the first and second values respectively. After that, because of the rest parameter's presence, `arr` gets the rest of the values in array form.
It only works if it's the last variable in the list.

Exercise: use destructuring assignment with the rest parameter to perform an effective `Array.prototype.slice()` so that `arr` is a sub-array of the original array `source` with the first two elements omitted.

```js
const source = [1,2,3,4,5,6,7,8,9,10];

function removeFirstTwo(list) {
	const [a, b, ...arr] = list;
	return arr;
}

const arr = removeFirstTwo(source);
```