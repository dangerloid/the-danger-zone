---
aliases:
tags: study
---
[[JavaScript]]
# JS Debugging - Prevent Infinite Loops with a Valid Terminal Condition
Loops are great tools when you need your program to run a code block a certain number of times until a condition is met, but they need a terminal condition that ends the looping. Infinite loops can freeze or crash the browser.

Example of infinite loop:

```js
function loopy() {
	while(true) {
		console.log('Hello, world!')
	}
}
```

It's the programmer's job to ensure that the terminal condition is eventually reached. One error is incrementing or decrementing a counter variable in the wrong direction from the terminal condition. Another one is accidentally resetting a counter or index variable within the loop code instead of incrementing or decrementing it.