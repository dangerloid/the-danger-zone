---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Find Characters with Lazy Matching
In regular expressions, a greedy match finds the longest possible part of a string that fits the regex pattern and returns it as a match.
The alternative is called a lazy match, which finds the smallest possible part of the string that satisfies the regex pattern.

You can apply the regex `/t[a-z]*i/` to the string `titanic`. This regex is a pattern that starts with `t`. ends with `i` and has some letters in between.

Regular expressions are greedy by default, so the match will return `["titani"]`.

But you can use `?` to change it to lazy matching. `"titanic"` matched against the adjusted regex `/t[a-z]*?i/` returns `["ti"]`.

>[!NOTE]
>Parsing HTML with regular expressions should be avoided, but pattern matching an HTML string with regular expressions is fine.

Exercise: fix the regex `/<.*>` to return the html tag `<h1>` and not the text `<h1>Winter is coming</h1>`.

```js
let text = "<h1>Winter is coming </h1>";
let myRegex = /<.*?>/;
let result = text.match(myRegex);
```