---
aliases: 
tags: study
---
[[JavaScript]]
# Mathematical Operations

## Basic Math

Simple mathematical operations are pretty straight-forward and can be done in-line in a [[JS Variables|Variable]] like so:

#### addition

```javascript
var sum = 10 + 10;
console.log(sum); // output will be 20
```

#### subtraction

```javascript
const difference = 45 - 33;
console.log(difference); // output will be 12
```

#### multiplication

```javascript
const product = 8 * 10;
console.log(product); // output will be 80
```

#### division

```javascript
const quotient = 66 / 33;
console.log(quotient); // output will be 2
```

## Increment and Decrement

To increment a number means to add 1 to it.

```javascript
var myVar = 87;
myVar = myVar + 1; // 88
```

The quicker way to do this though is by using the `++` operator.

```javascript
var myVar = 87;
myVar++; // 88
```

To decrement, you do the same with the `--` operator.

```javascript
var myVar = 11;
myVar--; // 10
```

## Decimal Numbers

Also referred to as floating point numbers or floats.

```javascript
var myDecimal = 9.22;
```

#### multiplication of decimals

Works just like integers.

```javascript
const decProduct = 2.0 * 2.5;
console.log(decProduct); // output will be 5
```

#### division of decimals

```javascript
const decQuotient = 4.4 / 2.0;
console.log(decQuotient); // output will be 2.2
```

## Remainders

The remainder operator `%` gives the remainder of the division of two numbers.

```javascript
const remainder = 11 % 3;
console.log(remainder); // output will be 2
```

The remainder operator is often used to determine if a number is even or odd.

## Augmented Math Operations

#### compound assignment operators: addition 

You may want to add numbers like this:

```javascript
var a = 3;
a = a + 12;
```

This is a really common pattern, so you may want to use the `+=` operator as a shortcut.

```javascript
var compAdd = 3;
compAdd += 12; // output will be 15
```

#### compound assignment operators: subtraction

```javascript
var compSub = 11;
compSub -= 6; // output will be 5
```

#### compound assignment operators: multiplication

```javascript
var compMulti = 5;
compMulti *= 5; // output will be 25
```

#### compound assignment operators: division

```javascript
var compDiv = 48
compDiv /= 12;
```

## conditional (ternary) operator
The conditional operator can be used as a one line if-else expression.

The syntax is `a ? b : c`, where `a` is the condition, `b` is the code to run when the condition is `true` and `c` is the code to run when the condition is `false`.

Exercise: use the conditional operator in the `checkEqual` function to check if two numbers are equal or not. The function should return either the string `Equal` or `Not Equal`.

```js
function checksEqual(a, b) {
	return a === b ? "Equal" : "Not Equal";
}
```

### multiple conditional operators
This function uses an `if`/`else if`/`else` structure with conditional operators:

```js
function findGreaterOrEqual(a, b) {
	return (a === b) ? "a and b are equal"
		: (a > b) ? "a is greater"
		: "b is greater";
}
```
It's considered good practice to write every condition on a separate line.

Exercise: in the `checkSign` function, use multiple conditional operators to check if a number is positive, negative or zero.

```js
function checkSign(num) {
	return (num > 0) ? "positive"
		 : (num < 0) ? "negative"
		 : "zero";
}
```