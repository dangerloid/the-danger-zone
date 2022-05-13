---
aliases:
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Check For The Presence on an Element With indexOf()
Since arrays can be mutated at any time, there's no guarantee about where a particular item will be on a given array, or if that element still exists.
JavaScript provides the `indexOf()` method, which allows us to quickly and easily check for the presence of an element on an array.
`indexOf()` takes an element as a parameter and when called, it returns the index of that element, or `-1` if the element doesn't exist.

Example:

```js
let fruits = ['apples', 'pears', 'oranges', 'peaches', 'pears'];

fruits.indexOf('dates'); // returns -1
fruits.indexOf('oranges'); // returns 2
fruits.indexOf('pears'); // returns 1, which is the first instance of 'pears'
```

Exercise: `indexOf()` can be incredibly useful for quickly checking the presence of an element on an array. We have defined a function `quickCheck` that takes an array and an element as arguments. Modify the function using `indexOf()` so that it returns `true` if the passed element exists on the array and `false` if it does not.

```js
function quickCheck(arr, elem) {
	if (arr.indexOf(elem) > -1) {
		return true;
	} else {
		return false;
	}
}

console.log(quickCheck(['squash', 'onions', 'shallots'], 'mushrooms'));
```