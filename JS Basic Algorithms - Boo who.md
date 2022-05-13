---
aliases:
tags: study
---
[[JS Basic Algorithm Scripting]]
# JS Basic Algorithms - Boo who
Check if a value is classified as a boolean primitive. Return `true` or `false`.

```js
function booWho(bool) {
	if (bool === true || bool === false) {
		return true;
	}
	return false;
}

booWho(null);
```

Alternate, cleaner solution:

```js
function booWho(bool) {
	return typeof bool === 'boolean';
}

booWho(null);
```