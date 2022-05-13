---
aliases:
tags: study
---
[[JS Basic Algorithm Scripting]]
# JS Basic Algorithms - Reverse a String
Reverse the string.

```js
function reverseString(str) {
	let newStr = "";
	for (let i = str.length -1; i >= 0; i--) {
		newStr += str[i];
	}
	return newStr;
}

reverseString('hello');
```