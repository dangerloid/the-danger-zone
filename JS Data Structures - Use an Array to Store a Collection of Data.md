---
aliases:
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Use an Array to Store a Collection of Data
The below is an example of the simples implementantion of an array data structure:

```js
let simpleArray = ['one', 2, 'three', true, false, undefined, null];
console.log(simpleArray.length); // displays 7
```

This is known as a *one-dimensional array*, meaning it only has one level or that is doesn't have any other nested arrays in it. It contains multiple different data types.

All arrays have a length property and can be accessed easily with `Array.length`.
A more complex implementation can be this:

```js
let complexArray = [
	[
		{
			one: 1,
			two: 2
		},
		{
			three: 3,
			four: 4
		},
	],
	[
		{
			a: 'a',
			b: 'b'
		},
		{
			c: 'c',
			d: 'd'
		}
	]
];
```

This is a multi-dimensional array. Specifically, this one contains objects.

Exercise: we have defined a variable called `yourArray`. Complete the statement by assigning an array of at least 5 elements in length to the `yourArray` variable. Your number should contain at least *one string*, *one number* and *one boolean*.

```js
let yourArray = [1, "two", 3, "four", false];
```