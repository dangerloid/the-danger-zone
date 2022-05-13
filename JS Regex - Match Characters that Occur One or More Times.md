---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Match Characters that Occur One or More Times
Sometimes you need to match a character or group of characters that appear one or more times in a row. To do that you use the `+` sign.

Exercise: you want to find matches when the letter `s` occurs one or more times in `Mississippi`. Write a regex that uses the `+` sign.

```js
let difficultSpelling = "Mississippi";
let myRegex = /s+/gi;
let result = difficultSpelling.match(myRegex);
```