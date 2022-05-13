---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Match Beginning String Patterns
Carets are used to negate character sets. Outside of a character set the caret is used to search for patterns at the beginning of strings.

```js
let firstString = "Ricke is first and can be found.";
let firstRegex = /^Ricky/;
firstRegex.test(firstString); // returns true
let notFirst = "You can't find Ricky now.";
firstRegex.test(notFirst); // returns false
```

Exercise: use the caret character in a regex to find `Cal` only in the beginning of the string `rickyAndCal`.

```js
let rickyAndCal = "Cal and Ricky both like racing.";
let calRegex = /^Cal/;
let result = calRegex.test(rickyAndCal);
```