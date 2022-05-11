---
aliases:
tags: study
---
[[JavaScript]]
# JS Regex - Match Single Character Not Specified
You can also create a set of characters that you don't want to match. They are called negated characters.

To create a negated character you place a caret `^` after the opening bracket.

Exercise: create a single regex that matches all characters that are not a number or a vowel.

```js
let quoteSample = '3 blind mice';
let myRegex = /[^0-9aeiou]/gi;
let result = quoteSample.match(myRegex);
```