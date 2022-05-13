---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Match All Numbers
The shortcut to look for digits is `\d`. It's equal to `[0-9]`.

Exercise: use the shorthand character class `\d` to count how many digits are in movie titles. Written out numbers do not count.

```js
let movieName = "2001: A Space Odyssey";
let numRegex = /\d/g;
let result = movieName.match(numRegex).length;
```