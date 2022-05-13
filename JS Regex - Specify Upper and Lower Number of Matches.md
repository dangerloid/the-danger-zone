---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Specify Upper and Lower Number of Matches
You can use the `+` sing to look for [[JS Regex - Match Characters that Occur One or More Times|one or more characters]] and the asterisk to look for [[JS Regex - Match Characters that Occur Zero or More Times|zero or more characters]]. But sometimes you need to match a certain range of patterns.

You can specify the lower and upper numbers of patterns with quantity specifiers, which are defined with curly braces.

Example: to match only the letter `a` appearing between 3 and 5 times in the string `ah`:

```js
let A4 = 'aaaah';
let A2 = 'aah';
let multipleA /a{3,5}h/;
multipleA.test(A4); // returns true
multipleA.test(A2); // returns false
```

Exercise: change the regex `ohRegex` to match the entire phrase `Oh no` only when it has 3 to 6 letter `h`'s.

```js
let ohStr = "Ohhh no";
let ohRegex = /Oh{3,6} no/;
let result = ohRegex.test(ohStr);
```