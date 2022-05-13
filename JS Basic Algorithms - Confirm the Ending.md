---
aliases:
tags: study
---
[[JS Basic Algorithm Scripting]]
# JS Basic Algorithms - Confirm the Ending
Check if a string (`str`) ends with the given target string (`target`).

```js
function confirmEnding(str, target) {
	return str.slice(-target.length) === target; // If a negative number is provided as the first parameter to slice(), the offset is taken backwards from the end of the string.
}

confirmEnding("Bastian", "n");
```