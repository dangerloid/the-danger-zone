---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Check For Mixed Grouping of Characters
Sometimes we want to check for groups of characters using a regular expression and to achieve that we use parentheses.

If you want to find either `Penguin` or `Pumpkin` in a string, you can use the following: `/P(engu|upmk)in/g` then check whether the desired string groups are in the test string by using the `.test()` method.

```js
let testStr = 'Pumpkin';
let testRegex = /P(engu|umpk)in/g;
testRegex.test(testStr); // returns true
```

Exercise: fix the regex so that it checks the names of `Franklin Roosevelt` or `Eleanor Roosevelt` in a case sensitive manner and it should make concessions for middle names.
Then fix the code so that the regex that you have created is checked against `myString` and either `true` or `false` is returned depending on whether the regex matches.

```js
let myString = 'Eleanor Roosevelt';
let myRegex = /(Franklin|Eleanor).*Roosevelt/g;
let result = myRegex.test(myString);
```