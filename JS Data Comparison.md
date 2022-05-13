---
aliases: [==, ===, "!=", "!=="]
tags: study
---
[[JS Basics + ES6 Features]]
# JS Data Comparison

## equality operator
The equality operator `==` compares two values and returns `true` if they're equivalent or `false` if they're not.
==Equality != [[JS Assignment Operators|assignment]]==

Let's see an example:

```js
function equalityTest(myVal) {
	if (myVal == 10) {
		return "Equal";
	}
	return "Not Equal";
}
```

If `myVal` is equal to 10, return `"Equal"`. Otherwise, return `"Not Equal"`.
In order for JavaScript to compare two different data types it must convert one type to the other. This is known as Type Coercion.

My example:

```js
function testEqual(val) {
	if (val == 12) { 
		return "Equal";
	}
	return "Not Equal";
}
```

## strict equality operator `===`

Strict equality is the counterpart to the equality operator, but unlike it, which converts both values to the same data type, the strict equality operator doesn't perform a type conversion, meaning that to be equal, the values need to be of the same type. 

Example:

```js
function testStrict(val) {
	if (val === 7) {
		return "Equal";
	}
	return "Not Equal";
}
```

## inequality operator `!=`
The inequality operator is the opposite of the equality operator. It returns `false` where equality would return `true` and viceversa. The inequality operator will convert data types when comparing.

```javascript
function testNotEqual(val) {
	if (val != 99) {
		return "Not Equal";
	}
	return "Equal";
}
```

## strict inequality operator `!==`

The strict inequality operator is the logical opposite of the strict equality operator. I doesn't perform type conversion when comparing.

```javascript
function testStrictNotEqual(val) {
	if (val !== 17) {
		return "Not Equal";
	}
	return "Equal";
}
```

## greater than operator `>`

The greater than operator compares the value of two [[JS Number|numbers]]. If the number to the left is greater than the number to the right, it returns `true`.

Example:

```javascript
function testGreaterThan(val) {
	if (val > 100) {
		return "Over 100";
	}
	if (val > 10) {
		return "Over 10";
	}
	return "10 or Under"
}
```

### greater than or equal operator `>=`

The greater than or equal operator compares the value of two numbers. If the number to the left is greater than or equal to the number on the right, it returns `true`.

Example:

```javascript
function testGreaterOrEqual(val) {
	if (val >= 20) {
		return "20 or Over";
	}
	if (val >= 10) {
		return "10 or Over";
	}
	return "Less than 10";
}
```

## less than operator `<`

The less than operator compares the value of two numbers. If the number to the left is less than to the number on the right, it returns `true`.

```javascript
function testLessThan(val) {
	if (val < 25) {
		return "Under 25";
	}
	if (val < 55) {
		return "Under 55";
	}
	return "55 or Over";
}
```

### less than or equal operator `<=`

The less than operator compares the value of two numbers. If the number to the left is less than to the number on the right, it returns `true`.

```javascript
function testLessThan(val) {
	if (val <= 12) {
		return "Smaller Than or Equal to 12";
	}
	if (val <= 24) {
		return "Smaller Than or Equal to 24";
	}
	return "More Than 24";
}
```

## logical AND `&&`

Sometimes testing multiple things at once is necessary. The *logical and* operator `&&` returns `true` if the operands to the left and right of it are true. It can also be done by nesting an `if` statement inside another.

```js
if (val <= 50 && val >= 25) {
	return "Yes";
}
return "No";
```

## logical OR `||`

The *logical or* operator `||` returns `true` if either of the operands is true.

```js
if (val < 10 || val > 20) {
	return "Outside";
}
return "Inside";
```

#### related notes

[[JS Functions#use conditional logic with if statements]]