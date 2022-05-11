---
aliases:
tags: study
---
[[JavaScript]]
# JS Regex - Match Single Character with Multiple Possibilities
Literal and wildcard characters in regular expressions are the extremes, where one finds exact matches and the other matches everything.

You can search for a literal pattern with some flexibility with character classes. They allow you to define a group of characters you want to match by placing them inside square brackets.

Example: you want to match `big`, `bag` and `bug` but not `bog`.

```js
let bigStr = "big";
let bagStr = "bag";
let bugStr = "bug";
let bogStr = "bog";
let bgRegex = /b[aiu]g/;
bigStr.match(bgRegex);
bagStr.match(bgRegex);
bugStr.match(bgRegex);
bogStr.match(bgRegex); // returns null
```

Exercise: use a character class with vowels in your regex to find all the vowels in the string.

```js
let quoteSample = "Beware of bugs in the above code; I have only proved it correct, not tried it.";
let vowelRegex = /[aeiou]/gi;
let result = quoteSample.match(vowelRegex);
```