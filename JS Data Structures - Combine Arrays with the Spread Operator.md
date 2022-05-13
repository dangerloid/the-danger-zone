---
aliases:
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Combine Arrays with the Spread Operator
Another advantage of using the spread operator is the ability to combine arrays, or insert all the elements of one array into another at any index.
We can concatenate arrays with traditional syntax, but this only allows us to combine arrays at the end of one.

Example of combined array with spread syntax:

```js
let thisArray = ['sage', 'rosemary', 'parsley', 'thyme'];
let thatArray = ['basil', 'cilantro', ...thisArray, 'coriander'];
```

Using spread syntax we have achieved an operation that would have been more complex and more verbose has we used traditional methods.

Exercise: we have defined a function `spreadOut` that returns the variable `sentence`. Modify the function using the spread operator so that it returns the array `['learning', 'to', 'code', 'is' 'fun']`.

```js
function spreadOut() {
	let fragment = ['to', 'code'];
	let sentence = ['learning', ...fragment, 'is', 'fun'];;
	return sentence;
}

console.log(spreadOut());
```