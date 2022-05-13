---
aliases:
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Copy Array Items Using slice()
Rather than modifying an array, `slice()` copies or extracts a given number of elements to a new array, leaving the array it's called upon untouched.
`slice()` takes only 2 parameters - the first is the index at which to begin extraction, the second is the index at which to stop extraction.
Extraction will occur up to but not including the element at the end index.

Example:

```js
let weatherConditions = ['rain', 'snow', 'sleet', 'hail', 'clear']; // unchanged

let todaysWeather = weatherConditions.slice(1, 3); // value is ['snow', 'sleet']
```

In effect, we have created a new array by extracting elements from an existing array.

Exercise: we have defined a function `forecast` that takes an array as an argument. Modify the function using `slice()` to extract information from the argument array and return a new array that contains the string elements `warm` and `sunny`.

```js
function forecast(arr) {
	return arr.slice(2, 4);
}

console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```