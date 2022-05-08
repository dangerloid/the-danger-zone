---
aliases:
tags: study
---
[[JS Methods]]
# JS parseInt() function
The `parseInt()` function parses a string and returns an integer.

## use the parseInt() function

Example: this function converts the string `007` into the integer 7. If the first character in the string can't be converted into a number, it returns `NaN`.

```js
const a = parseInt("007");
```

Exercise: use `parseInt()` in the `convertToInteger` function so that it converts the input `str` into an integer and returns it.

```js
function convertToInteger(str) {
	let int = parseInt(str);
	return int;
}
```

## use the parseInt() function with a radix
The  `parseInt()` function parses a string and returns an integer. It takes a second argument for the radix, which specifies the base of the number in the string. It can be an integer between 2 and 36.

Exercise: use `parseInt()` in the `convertToInteger` function so it converts a binary number to an integer and returns it.

```js
function convertToInteger(str) {
	let bin = parseInt(str, 2);
	return bin;
}
```