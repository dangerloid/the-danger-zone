---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Match a Literal String with Different Possibilities
The regex `/coding/` is going to search for the pattern `coding` in a string.
It's powerful for searching single strings, but is limited to only one pattern. You can search for multiple patterns using the alternator or `OR` operator `|`.

This operator matches patterns either before or after it.

Exercise: complete the regex `petRegex` to match the pets `dog`, `cat`, `bird` or `fish`.

```js
let petString = "James has a pet cat.";
let petRegex = /dog|cat|bird|fish/;
let result = petRegex.test(petString);
```