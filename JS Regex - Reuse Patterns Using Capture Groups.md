---
aliases:
tags: study
---
[[JavaScript]]
# JS Regex - Reuse Patterns Using Capture Groups
Say you want to match a word that occurs multiple times. You could use `/row row row/`, but what if you don't know the specific word repeated? Capture groups can be used to find repeated substrings.

Capture groups are constructed by enclosing the regex pattern to be captured in parentheses. In this case, the goal is to capture a word consisting of alphanumeric characters so the capture group will be `\w+` enclosed by parentheses `/(\w+)/`.

The substring matched by the group is saved to a temporary "variable" which can be accessed within the same regex via backslash and the number of the capture.
Capture groups are automatically numbered by the position of their opening parentheses starting at 1.

Example: this matches a word that occurs thrice separated by spaces.

```js
let repeatStr = "row row row your boat";
let repeatRegex = /(\w+) \1 \1/;
repeatRegex.test(repeatStr); // returns true
repeatStr.match(repeatRegex); // returns ["row row row", "row"]
```

Exercise: use capture groups in `reRegex` to match a string that consists of only the same number repeated exactly three times separated by single spaces.

```js
let repeatNum = "42 42 42";
let reRegex = /^(\d+)\s\1\s\1$/;
let result = reRegex.test(repeatNum);
```