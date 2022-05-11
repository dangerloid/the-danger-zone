---
aliases:
tags: study
---
[[JavaScript]]
# JS Regex - Match Everything But Letters and Numbers
You can search for the opposite with `\W`. It's equal to `[^A-Za-z0-9_]`.

```js
let shortHand = /\W/;
let numbers = "42%";
let sentence = "Coding!";
numbers.match(shortHand); // returns ["%"]
sentence.match(shortHand); // returns ["!"]
```

Exercise: use the shorthand character `\W` to count the number of non alphanumeric characters in various quotes and strings.

```js
let quoteSample = "The five boxing wizards jump quickly.";
let nonAlphabetRegex = /\W/g;
let result = quoteSample.match(nonAlphabetRegex).length;
```