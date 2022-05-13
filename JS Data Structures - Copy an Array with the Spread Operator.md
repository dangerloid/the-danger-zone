---
aliases:
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Copy an Array with the Spread Operator
While `slice()` allows us to be selective about what elements of an array to copy, the spread operator allows us to easily copy all of an array's elements, in order, with a simple and highly readable syntax: `...arr`.

Example:

```js
let thisArray = [true, true, undefined, false, null]; // unchanged
let thatArray = [...thisArray]; // copy of thisArray
```

Exercise: we have defined a function `copyMachine` which takes `arr` and `num` as arguments. The function is supposed to return a new array made up of `num` copies of `arr`. Modify the function using spread syntax so that it works correctly.

```js
function copyMachine(arr, num) {
	let newArr = [];
	while (num >= 1) {
	let obj = [...arr];
	newArr.push(obj);
	num--;
	}
	return newArr;
}

console.log(copyMachine([true, false, true], 2));
```