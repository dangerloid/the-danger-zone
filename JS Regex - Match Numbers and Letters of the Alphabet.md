---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Match Numbers and Letters of the Alphabet
Using the hyphen to match a range of characters is not limited to letters.

For example: `/[0-5]/` will match any number between 0 and 5.

Example of combining a range of letters and numbers in one character set:

```js
let jennyString = "Jenny8675309";
let myRegex = /[a-z0-9]/;
jennyStr.match(myRegex);
```

Exercise: create a single regex that matches a range of letters between h and s and a range of numbers between 2 and 6.

```js
let quoteSample = "Blueberry 3.141592653s are delicious."
let myRegex = /[h-s2-6]/gi;
let result = quoteSample.match(myRegex):
```