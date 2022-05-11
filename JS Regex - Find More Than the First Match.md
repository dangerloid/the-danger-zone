---
aliases:
tags: study
---
[[JavaScript]]
# JS Regex - Find More Than the First Match
So far, every regex I've written returned the first match it found.

To search or extract a pattern more than once, you can use the `g` flag.

Example:

```js
let testStr = "Repeat, Repeat, Repeat";
let repeatRegex = /Repeat/g;
testStr.match(repeatRegex); // returns all instances of 'Repeat'
```

Exercise: using the regex `starRegex` find and extract both `Twinkle` words from the string `twinkleStar`.

```js
let twinkleStar = "Twinkle, twinkle, little star";
let starRegex = /twinkle/gi;
let result = twinkleStar.match(starRegex);
```