---
aliases: .test()
tags: study
---
[[JavaScript]]
# JS Regex - Using the Test Method
Regular expressions are used in programming languages to match parts of strings.

If you want to find the word `the` in the string `The dog chased the cat`, you could use the following: `/the/`. Quote marks are not required.

A way to test a regex in JavaScript is to use the `test()` method. It takes the regex, applies it to a string which variable is assigned to is going to be passed as the parameter, and returns true or false if your pattern finds something or not.

```js
let testStr = "freeCodeCamp";
let testRegex = /Code/;
testRegex.test(testStr); // returns true
```

Exercise: apply the regex `myRegex` on the string `myString` using the `test()` method.

```js
let myString = "Hello, World!";
let myRegex = /Hello/;
let result = myRegex.test(myString);
```