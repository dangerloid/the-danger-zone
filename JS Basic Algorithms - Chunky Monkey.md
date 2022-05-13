---
aliases:
tags: study
---
[[JS Basic Algorithm Scripting]]
# JS Basic Algorithms - Chunky Monkey
Write a function that splits an array into groups the length of `size` and returns them as two-dimensional arrays.

```js
function chunkArrayInGroups(arr, size) {
	let newArray = [];
	for (let i = 0; i < arr.length; i += size) {
		newArray.push(arr.slice(i, i + size));
	}
	return newArray;
}

chunkArrayInGroups(["a", "b", "c", "d"], 2);
```