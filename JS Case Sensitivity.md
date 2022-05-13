---
aliases: camelCase
tags: study
---
[[JS Basics + ES6 Features]]
# Case Sensitivity

Capitalization matters in variable names.
If a variable is assigned and then declared, but the capitalization doesn't match, the debug console will output an error, because it counts it as two distinct variables and the second one hasn't been declared.

Example: 

```javascript
// declaration
var myVar;

// assignment
myVar = 10;
```

Best practice recommends using camelCase, where the first word is all lowercase and from the second word onward the first letter is capitalized.