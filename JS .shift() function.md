---
aliases: .shift()
tags: study
---
[[JS Arrays]]
# JS .shift() function

`.shift()` is similar to `.pop()`, but it removes the first element of an array.

```javascript
const myArray = [["John", 23], ["dog", 3]];
const removedFromMyArray = myArray.shift();
```

`removedFromMyArray` is now equal to `["John", 23]` and `myArray` equals to `["dog", 3]`.