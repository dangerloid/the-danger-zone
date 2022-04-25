---
aliases:
tags: study
---
[[JavaScript]]
# JS Functions

In JavaScript we can divide up our code into reusable parts called *functions*.

Syntax:

```js
function ourReusableFunction() {
	console.log("Heyya, World");
}

ourReusableFunction();
```

- `function`: defines the beginning of a function.
- `ourReusableFunction`: the name of the function.
- **parentheses**: the parameters go here.
- **curly brackets**: define the scope of the function. Every bit of code inside is related to it.
- `ourReusableFunction()`: calls the function, so that it runs. Without it, the function won't run. The amount of times the function is called (or invoked) defines how many times the code runs.

My example:

```js
function reusableFunction() {
	console.log("Hi World");
}

reusableFunction();
```

## passing values to functions with arguments

Parameters are variables that act as placeholders for the values that are to be input into a function when it is called.

When a function is defined, it is typically defined along with one or more parameters. The values that are passed into it when it's invoked are called *arguments*.

This function I wrote accepts two arguments and outputs the sum.

```js
function functionWithArgs(num1, num2) {
	console.log(num1 + num2);
}

functionWithArgs(2, 2); // outputs 2
functionWithArgs(15, 18); // outputs 33
```

## global scope and functions

"Scope" refers to the visibility of [[JS Variables|variables]]. Variables defines outside of a function block have global scope, meaning they can be seen throughout the whole program.

Variables declared without `let` or `const` are automatically created in the global scope. It is advisable to always declare a variable with a keyword, because this can create unintended consequences elsewhere in the code or when running a function again.

Example:

```js
let myGlobal = 10;

function fun1() {
	oopsGlobal = 5;
}

function fun2() {
	var output = "";
	if (typeof myGlobal != "undefined") {
		output += "myGlobal: " + myGlobal;
	}
	if (typeof != "undefined") {
		output += " oopsGlobal: " + oopsGlobal;
	}
}
```

`oopsGlobal` is in a function, but since it's been declared without a keyword, it will be treated as a global variable.

## local scope and functions

Variables declared in a function, as well as the parameters have local scope. This means that they're only visible inside the function.

Calling a variable outside of its scope will cause an error.

```js
function myLocalScope() {
	let myVar = 10;
	console.log(myVar);
}

myLocalScope();

console.log(myVar); // outputs an error `myVar is not defined`
```

## global vs. local scope in functions

It's possible to have local and global variables with the same name. When you do this, the local variable is prioritized.

```js
const outerWear = "T-shirt";

function myOutfit() {
	let outerWear = "sweater";
	return outerWear;
}

myOutfit(); // outerWear will be overridden with "sweater"
```

## return a value from a function with `return`

We can pass values into a function with [[JS Functions#passing values to functions with arguments|arguments]]. You can use a `return` statement to send a value back out of a function.

Example:
This function gets a `num` argument that gets multiplied by five.

```js
function timesFive(num) {
	return num * 5;
}

const product = timesFive(5); // outputs 25
```

## assignment with a returned value

We can assign a returned value to a variable.

```js
let processed = 0;

function processArg(num) {
	return (num + 3) / 5;
}

processed = processArg(7);
```

## stand in line (fCC exercise, queues)

A *queue* in computer science is an abstract data structure where items are kept in order.

This function adds an item to `testArr`, removes the first one and returns it.

My solution:
```js
const testArr = [1, 2, 3, 4, 5];

function nextInLine(arr, item) {
	arr.push(item);
	item = arr.shift();
	return item;
}
```

Another solution with less code:

```js
const testArr = [1, 2, 3, 4, 5];

function nextInLine(arr, item) {
	arr.push(item);
	return arr.shift();
}
```

## understanding boolean values

Another data type is the [[Boolean]]. They only have two values, `true` and `false`.

```js
function welcomeToBoolean() {
	return true; // no quotes, true and false aren't strings
}
```

## use conditional logic with if statements

An `if` statement is used to make decisions in code. `if` tells JavaScript to execute the code in the curly braces under conditions defined the the parentheses. These conditions are boolean and may only be `true` or `false`.

When the conditions evaluates to `true`, the code is executed, if it's `false` it will not be executed.

```js
function trueOrFalse(wasThatTrue) {
	if (wasThatTrue) {
		return "Yes, that was true";
	}
	return "No, that was false";
}
```

