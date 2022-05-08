---
aliases: while, for, loops, loop
tags: study
---
[[JavaScript]]
# JS Iteration
You can run the same code multiple times by using a loop.
## iterate with javascript while loops
`while` loops run while a specific condition is true and stops once it's no longer true.

Example: the `while` loop will execute 5 times and append the numbers o through 4 to `ourArray`.

```js
const ourArray = [];
let i = 0;

while (i < 5) {
	ourArray.push(i);
	i++
}
```

My example: add the numbers 5 through 0 in descending order to `myArray` using a while loop.

```js
const myArray = [];
let i = 5;

while (i >= 0) {
	myArray.push(i);
	i--;
}

// result will be myArray = [5, 4, 3, 2, 1, 0]
```

## iterate with javascript for loops
The most common type of JavaScript loop is called a `for` loop. It runs for a specific number of times.

For loops are declared with three optional expressions separated by semicolons:

`for (a; b; c;)`, where `a` is the initialization statement, `b` is the condition statement and `c` is the final expression.

The initialization statement is executed one time only before the loop starts. Typically used to set the variable for the loop.

The condition statement is evaluated at the beginning of every loop iteration and will continue as long as it evaluates to `true`. When the condition is false at the stare od the iteration the loop will stop. If the condition starts as false, the loop will never execute.

The final expression is executed at the end of each loop iteration, prior to the next condition check and is usually used to increment or decrement the loop counter.

Example: in this loop we initialize with `i = 0` and iterate while our condition `i < 5` is true.

```js
const ourArray = [];

for (let i = 0; i < 5; i++;) {
	ourArray.push(i);
}

// result is ourArray = [0, 1, 2, 3, 4]
```

My example: use a `for` loop to push the values 1 through 5 onto `myArray`.

```js
const myArray = [];

for (let i = 1; i <= 5; i++) {
	myArray.push(1);
}

// result is myArray = [1, 2, 3, 4, 5]
```

### iterate odd numbers with a for loop
For loops don't have to iterate one at a time. By changing the final expression we can count by even numbers.

My example: push the odd numbers 1 through 9 using a `for` loop.

```js
const myArray = [];

for (let i = 1; i <= 9; i += 2) {
	myArray.push(i);
}

// returns myArray = [1, 3, 5, 7, 9]
```

### count backwards with a for loop
A for loop can count backwards.

In order to decrement by two each iteration, we'll need to change our initialization, condition and final expression.

Exercise: push the odd numbers from 9 through 1 using a for loop.

```js
const myArray = [];

for (let i = 9; i >= 1; i -= 2) {
	myArray.push(i);
}
```

### iterate through an array with a for loop
A common task in JavaScript is to iterate through the contents of an array. One way to do this is with a `for` loop.

Exercise: declare and initialize a variable `total` to 0. Use a `for` loop to add the value of each element of `myArr` to `total`.

```js
const myArr = [2, 3, 4, 5, 6];

let total = 0;

for (let i = 0; i < myArr.length; i++) {
	total += myArr[i];
}
```

### nesting for loops
If you have a multidimensional array, you can use the same logic as the exercise above to loop through both the array and any sub-arrays.

Example: the output each sub-elements in `arr` one at a time.

```js
const arr = [
	[1, 2], [3, 4], [5. 6]
];

for (let i = 0; i < arr.length; i++) {
	for (let j = 0; j < arr[i].length; j++) {
		console.log(arr[i][j]);
	}
}
```

Exercise: modify function `multiplyAll` so that it returns the product of all the numbers in the sub-arrays of `arr`.

```js
function multiplyAll(arr) {
	let product = 1;
	for (let i = 0; i < arr.length; i++) {
		for (let j = 0; j < arr.length; j++) {
			product *= arr[i][j];
		}
	}
}
```

## iterate with javascript do...while loops
The next type of loop is the `do...while` loop.
It's called `do...while` because it will `do` one pass of the code no matter what and then continue `whule` the specified condition evaluates to `true`.

Example: this is similar to other iteration methods and the result will be an array that goes from 0 to 4.

```js
const ourArray = [];
let i = 0;

do {
	ourArray.push(i);
	i++;
} while (i < 5);
```

The difference between this and other loops is in how it behaves when it fails on first check. 

```js
const ourArray = [];
let i = 5;

while (i < 5) {
	ourArray.push(i);
	i++;
}
```

When we execute this `while` loop, the condition evaluates to `false` because `i` is not less than 5. `ourArray` will end up with no values.

The `do...while` loop above has the same. An `i` variable initialized to 5 and a condition that says to execute the code while the value of `i` is less than 5. But because there's no condition to evaluate during the first pass of the loop, it will execute correctly and the value of the array is `[5]`.

Exercise: change the `while` loop in the code to a `do...while` loop so that the loop will push only the number 10 to `myArray`, and `i` will be equal to 11 when your code finished running.

```js
const myArray = [];
let i = 10;

do {
	myArray.push(i);
	i++;
} while (i <= 10);
```

## replace loops using recursion
Recursion is the concept that a function can be expressed in terms of itself.

Example: multiply the first `n` elements of an array to create the product of those elements.

With a `for` loop:

```js
function multiply(arr, n) {
	let product = 1;
	for (let i = 0; i < n; i++) {
		product *= arr[i];
	}
	return product;
}
```

`multiply(arr, n) == multiply(arr, n - 1) * arr[n - 1]`. This means that you can write `multiply` in terms of itself and without needing a loop.

```js
function multiply(arr, n) {
	if (n <= 0) {
		return 1;
	} else {
		return multiply(arr,n - 1) * arr[n - 1];
	}
}
```
In the base case where `n <= 0`, it returns 1. For larger values of `n`, it calls itself but with  `n - 1`. Then it's evaluated the same way.

Exercise: write a recursive function `sum(arr, n)` that returns the sum of the first `n` elements of an array `arr`.

```js
function sum(arr, n) {
	if (n <= 0) {
		return 0;
	} else {
		return sum(arr, n - 1) + arr[n - 1];
	}
}
```

## profile lookup (fcc exercise)
We have an array of objects representing a contact list and a `lookupProfile` function that takes `name` and `prop` as arguments.

The function should check if `name` is an actual contact's `firstName` and the given `prop` is a property of that contact.

If both are true, then return the value of that property.

If `name` does not correspond to any contacts then return the string `No such contact`.

If `prop` does not correspond to any valid properties of a contact found to match `name`, then return the string `No such property`.

```js
function lookupProfile(name, prop) {
	for (let i = 0; i < contacts.length; i++) {
		if (contacts[i].firstName === name) {
			return contacts[i][prop] || "No such property";
		}
	}
	return "No such contact";
}
```

## use recursion to create a countdown
Let's write a complex function that returns an array of consecutive integers starting with 1 through the number passed to the function.

There will be a base case. It tells the recursive function when it no longer needs to call itself. It's a simple case where the value is already known.

Example: you want to write a recursive function that returns an array containing the numbers 1 through `n`. This function will need to accept the argument `n`, representing the final number. Then it will need to call itself with progressively smaller values of n until it reaches 1.

```js
function countup(n) {
	if (n < 1) {
		return [];
	} else {
		const countArray = countup(n - 1);
		countArray.push(n);
		return countArray;
	}
}

countup(5);

// returns [1, 2, 3, 4, 5]
```

Exercise: we have defined a function called `countdown` with one parameter (`n`). The function should use recursion to return an array containing the integers `n` through `1` based on the `n` parameter. If the function is called with a number less than 1, the function should return an empty array. For example, calling this function with `n = 5` should return the array `[5, 4, 3, 2, 1]`. Your function must use recursion by calling itself and must not use loops of any kind.

```js
function countdown(n){
	if (n < 1) {
		return [];
	} else {
		const arr = countdown(n - 1);
		arr.splice(0, 0, n);
		return arr;
	}
}
```

## use recursion to create a range of numbers
Exercise: we have defined a function named `rangeOfNumbers` with two parameters. The function should return an array of integers which begins with a number represented by the `startNum` parameter and ends with a number represented by the `endNum` parameter. The starting number will always be less than or equal to the ending number. Your function must use recursion by calling itself and not use loops of any kind. It should also work for cases where both `startNum` and `endNum` are the same.

```js
function rangeOfNumbers(startNum, endNum) {
	if (endNum - startNum === 0) {
		return [startNum];
	} else {
		var numbers = rangeOfNumbers(startNum, endNum - 1);
		numbers.push(endNum);
		return numbers;
	}
}
```