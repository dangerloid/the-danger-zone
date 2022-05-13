---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Find One or More Criminals in a Hunt (exercise)
A group of criminals escaped from jail and run away, but you don't know how many. However you do know that they stay close together when they are around other people. You are responsible for finding all the criminals at once.

Write a greedy regex that finds one or more criminals within a group of other people. A criminal is represented by the capital letter `C`.

```js
let reCriminals = /C+/;
```