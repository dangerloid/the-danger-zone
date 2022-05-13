---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Match Ending String Patterns
You can search the end of strings using the dollar sign at the end of the regex.

```js
let theEnding = "This is a never ending story";
let storyRegex = /story$/;
storyRegex.test(theEnding); // returns true
let noEnding = "Sometimes a story will have to end";
storyRegex.test(noEnding); // returns false
```

Exercise: use the anchor character `$` to match the string `caboose` at the end of the string `caboose`.

```js
let caboose = "The last car on a train is the caboose";
let lastRegex = /caboose$/;
let result = lastRegex.test(caboose);
```