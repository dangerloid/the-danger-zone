---
aliases: .match()
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Extract Matches
We've been only checking if a pattern exists or not within a string. You can also extract the actual matches with the `.match()` method.

To use the `.match()` method, apply the method on a string and pass in the regex inside the parentheses.

Example: the first match would return `["Hello"]` and the second would return `["expressions"]`.

```js
"Hello, World!".match(/Hello/);
let ourStr = "Regular expressions";
let ourRegex = /expressions/;
ourStr.match(ourRegex);
```

Note that the `.match` syntax is the opposite of the `.test` method.

Exercise: apply the `.match()` method to extract the string `coding`.

```js
let extractStr = "Extract the word 'coding' from this string."
let codingRegex = /coding/;
let result = extractStr.match(codingRegex);
```