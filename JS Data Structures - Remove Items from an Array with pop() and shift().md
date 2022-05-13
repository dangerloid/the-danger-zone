---
aliases:
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Remove Items from an Array with pop() and shift()
Both `push()` and `unshift()` have corresponding methods that are nearly functional opposites: `pop()` and `shift()`.
Instead of adding, `pop()` removes an element form the end of the array and `shift()` removes an element from the start of the array.

The key difference between them and `push()` and `unshift()` is that neither method takes parameters, and each only allows an array to be modified by a single element at a time.

Examples:

```js
let greetings = ['whats up?', 'hello', 'see ya!'];

greetings.pop(); // removed 'see ya!'
```

```js
greetings.shift(); // removed 'whats up?'
```

We can also return the value of the removed element with either method like this:

```js
let popped = greeting.pop(); // value is 'hello'
```

Exercise: we have defined a function `popShift` which takes an array as an argument and returns a new array. Modify the function using `pop()` and `shift()` to remove the first and last elements to their corresponding variables, so that the returned array contains their values.

```js
function popShift(arr) {
	let popped = arr.pop();
	let shifted = arr.shift();
	return [shifted, popped];
}

console.log(popShift(['challenge', 'is', 'not', 'complete']));
```

### related notes
[[JS .pop() function|.pop()]]
[[JS .shift() function|.shift()]]