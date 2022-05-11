---
aliases:
tags: study
---
[[JavaScript]]
# JS Regex - Specify Exact Number of Matches
To specify a specific number of patterns, just have one number between the curly braces.

```js
let A4 = "haaaah";
let A3 = "haaah";
let A100 = "h" + "a".repeat(100) + "h";
let multipleHA = /ha{3}h/;
multipleHA.test(A4); // returns false
multipleHA.test(A3); // returns true
multipleHA.test(A100); // returns false
```

Exercise: change the regex `timRegex` to match the word `Timber` only when it has four letter `m`'s.

```js
let timStr = "Timmmmber";
let timRegex = /tim{4}ber/i;
let result = timRegex.test(timStr);
```