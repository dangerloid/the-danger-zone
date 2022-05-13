---
aliases:
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Add Items Using splice()
You can use the third parameter, comprised of one or more element, to add to the array.
This can be useful for quickly switching out an element, or a set of elements, for another.

```js
const numbers = [10. 11, 12, 12, 15];
const startIndex = 3;
const amountToDelete = 1;

numbers.splice(startIndex, amountToDelete, 13, 14);
console.log(numbers);
```

The second occurrence of 12 is removed and we added 13 and 14 at the same index. The `numbers` array would now be `[10, 11, 12, 13, 14, 15]`.

We begin with an array of numbers. Then, we pass this to `splice()`:
- the index at which to begin deleting elements (3)
- the number of the elements to be deleted (1)
- the remaining arguments (13, 14). inserted starting at the same index

Exercise: we have defined a function, `htmlColorNames`, which takes an array on HTML colors as an argument. Modify the function using `splice()` to remove the first elements of the array and add `"DarkSalmon"` and `"BlanchedAlmond"` in their respective places.

```js
function htmlColorNames(arr) {
	arr.splice(0, 2, 'DarkSalmon', 'BlanchedAlmond');
	return arr;
}

console.log(htmlColorNames(['DarkGoldenRod', 'WhiteSmoke', 'LavenderBlush', 'PaleTurquoise', 'FireBrick']));
```