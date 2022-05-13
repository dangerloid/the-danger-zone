---
aliases:
tags: study
---
[[JS Basic Algorithm Scripting]]
# JS Basic Algorithms - Find the Longest Word in a String
Return the length of the longest word in the provided sentence.
Function should return a number.

```js
function findLongestWordLength(str) {
	let words = str.split(' '); // turns str into an array of words
	let maxLength = 0; // keeps track of the maximum length

	for (let i = 0; i < words.length; i++) { // loops from 0 to the length of the array of words
		if (words[i].length > maxLength) { 
			maxLength = words[i].length;
		} // checks for the longest word by comparing the current word to the previous one and storing the new longest word
	}
	return maxLength; // returns the value of maxLength
}

findLongestWordLength("The quick brown fox jumped over the lazy dog");
```