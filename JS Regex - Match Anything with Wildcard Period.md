---
aliases:
tags: study
---
[[JavaScript]]
# JS Regex - Match Anything with Wildcard Period
Sometimes you won't know the exact characters in your patterns.

The wildcard character `.` will match any one character. You can use the wildcard character just like any other character in a regex.

Example:

```js
let humStr = "I'll hum a song";
let hugStr = "Bear hug";
let huRegex = /hu./;
// both return true
huRegex.test(humStr);
huRegex.test(hugStr);
```

Exercise: complete the regex `unRegex` so that it matches `run`, `sun`, `fun`, `pun`, `nun` and `bun`.

```js
let exampleStr = "Let's have fun with regular expressions!";
let unRegex = /.un/;
let result = unRegex.test(exampleStr);
```