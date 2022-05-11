---
aliases:
tags: study
---
[[JavaScript]]
# JS Regex - Use Capture Groups to Search and Replace
You can search and replace using `.replace()` on a string. The inputs for `.replace()` is first the regex pattern you want to search for. The second parameter is the string to replace the match or a function to do something.

```js
let wrongText = "The sky is silver.";
let silverRegex = /silver/;
wrongText.replace(silverRegex. "blue"); // returns "The sky is blue."
```

You can also access capture groups in the replacement string with dollar signs.

```js
"Code Camp".replace(/(\w+)\s(\w+)/ '$2 $1'); // returns "Camp Code"
```

Exercise: write a regex `fixRegex` using three capture groups that will search for each word in the string `one two three`. Then update the `replaceText` variable to replace `one two three` with `three two one` and assign the result to the `result` variable. Make sure you are utilizing capture groups in the replacement string using the dollar sign syntax.

```js
let str = "one two three";
let fixRegex = /(\w+)\s(\w+)\s(\w+)/;
let replaceText = "$3 $2 $1";
let result = str.replace(firRegex, replaceText);
```