---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Match Whitespace
You can search for whitespace using `\s`. This pattern not only matches whitespace, but also carriage return, tab, form feed and newline.
It's similar to `[ \r\t\f\n\v]`.

```js
let whiteSpace = 'Whitespace. Whitespace everywhere!'
let spaceRegex = /\s/g;
whiteSpace.match(spaceRegex); // returns [" ", " "]
```

Exercise: change the regex `countWhiteSpace` to look for multiple whitespace characters in a string.

```js
let sample = "Whitespace is important in separating words";
let countWhiteSpace = /\s/g;
let result = sample.match(countWhiteSpace);
```