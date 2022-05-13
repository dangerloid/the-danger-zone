---
aliases:
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Add Items to an Array with push() and unshift()
An array's length is not fixed. Arrays can be defined with a length of any number of elements, and elements can be added or removed over time.
We'll look at two methods with which we can programmatically modify an array, `Array.push()` and `Array.unshift()`.

Both methods take one or more elements as parameters and add those elements to the array method the method is being called on.
The `push()` method appends elements to the end of the array.
The `unshift()` method adds elements to the start of the array.

Example:

```js
let twentyThree = 'XXIII';
let romanNumerals = ['XXI', 'XXII'];

romanNumerals.unshift('XIX', 'XX');
romanNumerals.push(twentyThree);
```

The value of `romanNumerals` is now `['XIX', 'XX', 'XXI', 'XXII', 'XXIII']`.
We can also pass variables which allows us greater flexibility in dynamically modifying our array's data.

Exercise: we have defined a function `mixedNumbers` which we are passing an array as an argument. Modify the function using `push()` and `unshift()` to add `'I', 2, 'three` to the beginning of the array and `7, 'VIII', 9` to the end so that the returned array contains representations of the numbers 1-9 in order.

```js
function mixedNumbers(arr) {
	arr.unshift('I', 2, 'three');
	arr.push(7, 'VIII', 9);
	return arr;
}

console.log(mixedNumbers(['IV', 5, 'six']));
```

### related notes
[[JS .push() function|.push()]]
[[JS .unshift() function|.unshift()]]