---
aliases:
tags: study
---
[[JavaScript]]
# JS Regex - Check for All or None
Sometimes the patterns you want to search for may have parts of it that may not exist. However it may be important to check for them nonetheless.

You can specify the possible existence of an element with a question mark. This checks for zero or one of the preceding element.

Example: spelling of the word `color` in American and British English respectively.

```js
let american = "color";
let british = "colour";
let rainbowRegex = /colou?r/;
rainbowRegex.test(american);
rainbowRegex.test(british); // both return true
```

Exercise: change the regex `favRegex` to match both the American and British spelling of the word `favorite`.

```js
let favWord = 'favorite';
let favRegex = /favou?rite/;
let result = favRegex.test(favWord);
```