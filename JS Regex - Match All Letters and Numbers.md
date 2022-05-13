---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Match All Letters and Numbers
Using character classes, you can search for every letter of the alphabet with `[a-z]`. This particular character class is common enough that there's a shortcut for it.

The closest character class in JavaScript to match the alphabet is `\w`. It's equal to `[A-Za-z0-9_]`. This class matches upper and lowercase letters and numbers plus the underscore.

```js
let longHand = /[A-Za-z0-9_]+/;
let shortHand = /\w+/;
let numbers = "42";
let varNames = "important_var";
longHand.test(numbers);
shortHand.test(numbers);
longHand.test(varNames);
shortHand.test(varNames);
```

All four of these return `true`.

Exercise: use the shorthand character class `\w` to count the number of alphanumeric characters in various quotes and strings.

```js
let quoteSample = "The five boxing wizards jump quickly.";
let alphabetRegexV2 = /\w/gi;
let result = quoteSample.match(alphabetRegexV2).length;
```