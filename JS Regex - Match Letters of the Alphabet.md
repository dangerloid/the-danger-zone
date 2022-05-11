---
aliases:
tags: study
---
[[JavaScript]]
# JS Regex - Match Letters of the Alphabet
You can use character sets to specify a group of characters to match, but it's inefficient when you need to match a large range of characters.
There's a built-in feature that makes it simple: inside a character set you can use a hyphen to define a character range.

Example: this regex finds all lowercase letters between a and e.

```js
let catStr = 'cat';
let batStr = 'bat';
let matStr = 'mat';
let bgRegex = /[a-e]at/;
catStr.match(bgRegex);
batStr.match(bgRegex);
matStr.match(bgRegex); // returns null
```

Exercise: match all letters in the string `quoteSample`.

```js
let quoteSample = "The quick brown fox jumps over the lazy dog.";
let alphabetRegex = /[a-z]/gi;
let result = quoteSample.match(alphabetRegex);
```