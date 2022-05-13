---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Match All Non-Numbers
The shortcut for non-digit characters is `\D`. It's equal to `[^0-9]`.

Exercise: use the shorthand character class for non-digits `\D` to count how many non-digits are in movie titles.

```js
let movieName = "2001: A Space Odyssey";
let noNumRegex = /\D/g;
let result = movieName.match(noNumRegex).length;
```