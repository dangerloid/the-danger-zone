---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Match Literal Strings
The regex from before searched for a literal match of the string `Hello`.

Example: here a regex is going to search for a literal match for `Kevin`.

```js
let testStr = "Hello, my name is Kevin."
let testRegex = /Kevin/;
testRegex.test(testStr);
```

It's case sensitive.

Exercise: complete the regex `waldoRegex` to find `"Waldo"` in the string `waldoIsHiding` with a literal match.

```js
let waldoIsHiding = "Somewher Waldo is hiding in this text.";
let waldoRegex = /Waldo/;
let result = waldoRegex.test(waldoIsHiding);
```

### related notes
[[JS Case Sensitivity]]