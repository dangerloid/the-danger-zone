---
aliases:
tags: study
---
[[JS Basic Algorithm Scripting]]
# JS Basic Algorithms - Repeat a String
Repeat a given string `str` for `num` times. Return an empty string if `num` is not a positive number.

```js
function repeatStringNumTimes(str, num) {
	let repStr = "";
	for (let i = 0; i < num; i++) {
		repStr += str;
	}
	return repStr;
}

repeatStringNumTimes("abc", 3);
```