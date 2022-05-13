---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Match Non-Whitespace Characters
The shorthand for non-whitespace characters is `\S`. It's similar to `[^ \r\t\f\n\v]`.

```js
let whiteSpace = "Whitespace. Whitespace everywhere!";
let nonSpaceRegex = /\S/g;
whiteSpace.match(nonSpaceRegex).length; // returns 32
```

Exercise: change the regex `countNonWhiteSpace` to look for multiple non-whitespace characters in a string.

```js
let sample = "Whitespace is important in separating words";
let countNonWhiteSpace = /\S/g;
let result = sample.match(countNonWhiteSpace);
```