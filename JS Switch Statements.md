---
aliases: switch, case, break
tags: study
---
[[JS Basics + ES6 Features]]
# JS Switch Statements
A `switch` statement tests a value and can have multiple `case` statements which define various possible values. Statements are executed from the first matched `case` value until a `break` is encountered.

`case` values are tested with a [[JS Data Comparison#strict equality operator|strict equality operator]].
The `break` tells JavaScript to stop executing statements. If it's omitted, the next statement will be executed.

Example:

```js
switch(val) {
	case 1:
		answer = "alpha";
		break;
	case 2:
		answer = "beta";
		break;
	case 3:
		answer = "gamma";
		break;
	case 4:
		answer = "delta";
		break;
}
```

## adding a default option to `switch` statements
In a `switch` statement you may not be able to specify all possible values in `case` statements. You can add the `default` statement which will be executed if no matching `case` is found.

```js
function switchOfStuff(val) {
	let answer = "";

	switch(val) {
		case "a":
			answer = "apple";
			break;
		case "b":
			answer = "bird";
			break;
		case "c":
			answer = "cat";
			break;
		default:
			answer = "stuff";
			break;
	}
}

switchOfStuff(1); // returns "stuff"
```

## multiple identical options in `switch` statements
If the `break` statement is omitted, the following `case` are executed until a `break` is encountered.

This function returns `"Low"`, `"Mid"` or `"High"` based on the range in which the case is in.

```js
function sequentialSizes(val) {
	let answer = "";

	switch(val) {
		case 1:
		case 2:
		case 3:
			answer = "Low";
			break;
		case 4:
		case 5:
		case 6:
			answer = "Mid";
			break;
		case 7:
		case 8:
		case 9:
			answer = "High";
			break;
	}
	return answer;
}
sequentialSizes(1); // returns "Low"
```

## replacing `if else` chains with `switch` statements
If you have many options to choose from a `switch` statement can be easier to write than many chained `if`/`if else` statements.

Example from the exercise:

```js
function chainToSwitch(val) {
	let answer = "";

	if (val === "bob") {
		answer ="Marley";
	} else if (val === 42) {
		answer = "The Answer";
	} else if (val === 1) {
		answer = "There is no #1";
	} else if (val === 99) {
		answer = "Missed me by this much!";
	} else if (val === 7) {
		answer = "Ate Nine";
	}

	return answer;
}
```

This is convoluted and hard to read.
`switch` statements are cleaner and easier to write and read.

```js
function chainToSwitch(val) {
	let answer = "";

	switch(val) {
		case "bob":
			answer = "Marley";
			break;
		case 42:
			answer = "The Answer";
			break;
		case 1:
			answer = "There is no #1";
			break;
		case 99:
			answer = "Missed me by this much!";
			break;
		case 7:
			answer = "Ate Nine";
			break;
	}
	return answer;
}
```

## counting cards (fcc exercise)
In the game Blackjack, a player can gain an advantage over the house by keeping track of the relative number of high and low cards remaining in the deck. This is called **card counting**.

Having more high cards remaining in the deck favors the player. Each card is assigned a value. When the count is positive, the player should bet high. When the count is 0 or negative, they should bet low.

```js
let count = 0;

function cc(card) {
	switch(card) {
		case 2:
		case 3:
		case 4:
		case 5:
		case 6:
			count++;
			break;
		case 10:
		case 'J':
		case 'Q':
		case 'K':
		case 'A':
			count--;
			break;
	}

	var holdbet = 'Hold'
	if (count > 0) {
		holdbet = 'Bet'
	}
	return count + " " + holdbet;

}

cc(2); cc(3); cc(7); cc('K'); cc('A');
console.log(cc(4));
```

### related notes
[[JS Functions]]