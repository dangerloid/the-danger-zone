---
aliases:
tags: study
---
[[JavaScript]]
# JS Regex - Remove Whitespace from Start and End
Sometimes whitespace characters around strings are not wanted but are there. Typical processing of strings is to remove the whitespace at the start and end of it.

Exercise: write a regex and use the appropriate string method to remove whitespace at the beginning and end of strings.

The `String.prototype.trim()` method would work here, but you'll need to complete this challenge using regular expressions.

```js
let hello = " Hello, World! ";
let wsRegex = /^\s+|\+$/g;
let result = hello.replace(wsRegex, "");
```