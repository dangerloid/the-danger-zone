---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Positive and Negative Lookahead
Lookaheads are patterns that tell JavaScript to look-ahead in your string to check for patterns further along. This can be useful when you want to search for multiple patterns over the same string.

There are two kinds of lookaheads: positive and negative.

A positive lookahead will look to make sure the element in the search pattern is there, but won't actually match it. A positive lookahead is used a `(?=...)`, where `...` is the required part that's not matched.

A negative lookahead will look to make sure the element in the search pattern is not there. It's used as `(?!...)`. The rest of the pattern is returned if the negative lookahead part is not present.

Example:

```js
let quit = 'qu';
let noquit = 'qt';
let quRegex = /q(?=u)/;
let qRegex = /q(?!u)/;
quit.match(quRegex); // returns true
noquit.match(qRegex); // returns true
```

A more practical use of lookaheads is to check two or more patterns in one string. Here is a simple password checker that looks for between 3 and 6 characters and at least one number:

```js
let password = 'abc123';
let checkPass = /(?=\w{3,6}(?=\D*\d))/;
checkPass.test(password);
```

Exercise: use lookaheads in the `pwRegex` to match passwords that are greater than 5 characters long and have two consecutive digits.

```js
let sampleWord = 'astronaut';
let pwRegex = /(?=\w{6})(?=\w*\d{2})/gi;
let result pwRegex.test(sampleWord);
```