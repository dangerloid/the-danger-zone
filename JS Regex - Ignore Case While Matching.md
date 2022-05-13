---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Ignore Case While Matching
Case is the difference between uppercase letters and lowercase letters.
You can match both cases with the flag `i`, which is put at the end of the regex: `/ignorecase/i`.

Exercise: write a regex `fccRegex` to match `freeCodeCamp`, no matter its case. Your regex should not match any abbreviations or variations with spaces.

```js
let myString = "freeCodeCamp";
let fccRegex = /freeCodeCamp/i;
let result = fccRegex.test(myString);
```