---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Specify Only the Lower Number of Matches
Sometimes you only want to specify the lower number of matches with no upper limit.
To specify the lower number of patterns, keep the first number followed by a comma.

```js
let A4 = 'haaaah';
let A2 = 'haah';
let A100 = 'h' + 'a'.repeat(100) + 'h';
multipleA = /ha{3,}h/;
multipleA.test(A4); // returns true
multipleA.test(A2); // returns false
multipleA.test(A100); // returns true
```

Exercise: change the regex `haRegex` to match the word `Hazzah` only when it has four or more letter `z`'s.

```js
let haStr = "Hazzzzah";
let haRegex = /haz{4,}ah/gi;
let result = haRegex.test(haStr);
```