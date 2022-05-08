---
aliases:
tags: study
---
[[JS Methods]]
# JS Math.random() function
## generate random fractions with javascript
Random numbers are useful for creating random behavior.

To generate a random decimal number between 0 (inclusive) and 1 (exclusive), you can use `Math.random()`.

Exercise: change `randomFraction` to return a random number instead of 0.

```js
function randomFraction() {
	return Math.random();
}
```

## generate random whole numbers with javascript
Generating whole numbers is far more useful.

1. use `Math.random()` to generate a random decimal;
2. multiply that random decimal by 20;
3. use `Math.floor` to round it down to the nearest whole number.

`Math.random()` can never return a 1 and since we're rounding down, we can't get a 20.

Exercise: generate and return a random whole number between 0 and 9.

```js
function randomWholeNum() {
	return Math.floor(Math.random() * 10);
}
```

## generate random whole numbers within a range
We can generate a random whole number that falls in a range between two specific numbers.

To do this we define a minimum and a maximum number.

Formula:

```js
Math.floor(Math.random() * (max - min + 1)) + min 
```

Exercise: create a function called `randomRange` that takes a range `myMin` and `myMax` and returns a random whole number that's greater than or equal to `myMin` and is less than or equal to `myMax`, inclusive.

```js
function randomRange(myMin, myMax) {
	return Math.floor(Math.random() * (myMax - myMin + 1)) + myMin; 
}
```