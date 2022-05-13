---
aliases:
tags: study
---
[[JS Basic Algorithm Scripting]]
# JS Basic Algorithms - Truncate a String
Truncate a string if it is longer than the given maximum string length. Return the truncated string with a `...` ending.

```js
function truncateString(str, num) {
	if (str.length > num) {
		let shortStr = '';
		return shortStr = str.slice(0, num) + '...';
	}
	return str;
}

truncateString("A-tisket a-tasket A green and yellow basket", 8);
```