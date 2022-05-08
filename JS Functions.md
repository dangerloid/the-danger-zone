---
aliases: function, else, if, else if, switch
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
## `if`, `else`, `else if`
### understanding boolean values

Another data type is the [[JS Boolean]]. They only have two values, `true` and `false`.

```js
function welcomeToBoolean() {
	return true; // no quotes, true and false aren't strings
}
```

### use conditional logic with if statements

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

### `else` statements

When a condition for an `if` statement is true, the block of code following it is executed, while when it's not, nothing happens. With an `else` statement, an alternate block of code can be run.

```js
function testElse(val) {
	let result = "";
	if (val > 5) {
		result = "Bigger than 5";
	} else {
		result = "5 or Smaller";
	}
	return result;
}
```

### `else if` statements

When you have multiple conditions to be addressed, you can chain `if` statements with the `else if` keyword.

```js
function testElseIf(val) {
	if (val > 10) {
	return "Greater than 10";
	} else if (val < 5) {
	return "Smaller than 5";
	} else {
	return "Between 5 and 10";
	}
}
testElseIf(7);
```

### logical order in `if else` statements
The function is executed from top to bottom, so you want to be careful of what comes first.

Examples:

```js
function orderMyLogic(val) {
	if (val < 10) {
	return "Less than 10";
	} else if (val < 5) {
	return "Less than 5"
	} else {
	return "Greater than or equal to 10"
	}
}

orderMyLogic(7);
```
If we want to evaluate 3, we'll still going to get `Less than 10` in the console. To get `Less than 5` we're going to change the order.

```js
function orderMyLogic(val) {
	if (val < 5) {
	return "Less than 5";
	} else if (val < 10) {
	return "Less than 10"
	} else {
	return "Greater than or equal to 10"
	}
}

orderMyLogic(7);
```

### chaining `if else` statements
`if/else` statements can be chained together for complex logic.

Example:

```js
if (num < 5) {
return "Tiny";
} else if (num < 10) {
return "Small";
} else if (num < 15) {
return "Medium";
} else if (num < 20) {
return "Large";
} else if (num >= 20) {
return "Huge";
}
```

### golf code (fcc exercise)

Solution:

```js
const names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"];


function golfScore(par, strokes) {
	if (strokes == 1) {
	return names[0];
	} else if (strokes <= par - 2) {
	return names[1];
	} else if (strokes == par - 1) {
	return names[2];
	} else if (strokes == par) {
	return names[3];
	} else if (strokes == par + 1) {
	return names[4];
	} else if (strokes == par + 2) {
	return names[5];
	} else {
	return names[6];
	}
}
golfScore(5, 4);
```

## returning [[JS Boolean|boolean]] values from functions
All data comparisons return a boolean value. Sometimes people use an `if`/`else` statement to do a comparison:

```js
function isEqual(a, b) {
	if (a === b) {
		return true;
	} else {
		return false;
	}
}
```

But the better way to do this is not using it. For cleaner and more human-readable code, a comparison operator (strict equality in this case) is enough, because it will always return a boolean value when comparing.

```js
function isEqual(a, b) {
	return a === b;
}
```

Exercise:

```js
function isLess(a, b) {
	return a < b;
}
isLess(10, 15); // returns true
```

## return early pattern for functions
When a `return` statement is reached, the execution of the current function stops and control returns to the calling location.

This exercise requires a function that returns `undefined` if `a` or `b` are less than 0.

[[JS Undefined|undefined]] is a *keyword*, not a string.

```js
function abTest(a, b) {
	if(a < 0 || b < 0) {
		return undefined;
	}
	return Math.round(Math.pow(Math.sqrt(a) + Math.sqrt(b), 2));
}

abTest(2,2); // returns 8, not that it matters
```

## use arrow functions to write concise anonymous functions
In JavaScript we don't always need to name our functions, especially when passing a function as an argument to another function.
Instead we can write inline functions. They don't need to be named because we don't need to reuse them.

Syntax:

```js
const myFunc = function() {
	const myVar = "value";
	return myVar;
}
```

ES6 provides arrow function syntax, which makes for cleaner code and less redundancy. So the function above will be:

```js
const myFunc = () => {
	const myVar = "value";
	return myVar;
}
```

When there's no function body, like just returning a value, it can be even more streamlined:

```js
const myFunc = () => "value";
```

## write arrow functions with parameters
Arrow functions are just like regular functions, and they do take parameters.
If an arrow function has a single parameter, the parentheses are omitted.

Exercise: rewrite the following function which appends the contents of `arr2` to `arr1` so that the function uses arrow function syntax.

```js
// example func
var myConcat = function(arr1, arr2) {
	return arr1.concat(arr2);
}

// my solution
const myConcat = (arr1, arr2) => arr1.concat(arr2);
```
## write higher order arrow functions
Arrow functions work well with higher order functions like, `map`, `filter` and `reduce`.
They take functions as arguments for processing collections of data.
Whenever a function takes another function as an argument, it's recommended to use an arrow function.

Exercise: update the `squareList` function to compute the square of only the positive integers in the array.
```js
const realNumberArray = [4, 5.6, -9.8, 3.14, 42, 6, 8.34, -2];

const squareList = (arr) => {
	const squaredIntegers = arr.filter(num => Number.isInteger(num) && num > 0).map(x => x * x); 
	return squaredIntegers;
}

const squaredIntegers = squareList(realNumberArray);
```

## set default parameters for your functions
ES6 introduced default parameters for functions for flexibility.

Example:

```js
const greeting = (name = "Anonymous") => "Hello" + name;
```

The default parameter kicks in when the argument is not specified when the function is called.

Exercise: modify the function `increment` by adding default parameters so that it will add 1 to `number` if `value` is not specified.

```js
const increment = (number, value = 1) => number + value;
```

## use the rest parameter with function parameters
The rest parameter (`...`), like default parameters, were introduced in ES6 for flexibility's sake.
With them, you can create functions that take a variable number of arguments. They are then stored in an array that can be accessed later from the function.

Exercise: modify the function `sum` using the rest parameter
in such a way that the function `sum` is able to take any number of arguments and return their sum.

```js
const sum = (...args) => {
	return args.reduce((a, b) => a + b, 0);
}
```

## write concise declarative functions
When defining a function prior to ES6, we had the `function` keyword.

```js
const person = {
	name: "Taylor",
	sayHello: function() {
		return `Hello! My name is ${this.name}.`;
	}
};
```

With ES6. you can remove the `function` keyword and color when defining functions in objects.

```js
const person = {
	name: "Taylor",
	sayHello() {
		return `Hello! My name is ${this.name}.`;
	}
};
```

Exercise: refactor the function `setGear` inside the object `bicycle` to use shorthand syntax described above.

```js
const bicycle = {
	gear: 2,
	setGear(newGear) {
		this.gear = newGear;
	}
};

bicycle.setGear(3);
```

#### related notes
[[JS Switch Statements]]
[[JS Data Comparison]]