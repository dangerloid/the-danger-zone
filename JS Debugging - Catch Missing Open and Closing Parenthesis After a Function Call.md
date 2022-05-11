---
aliases:
tags: study
---
[[JavaScript]]
# JS Debugging - Catch Missing Open and Closing Parenthesis After a Function Call
When a function or method doesn't take any arguments, you may forget to include the opening and closing parentheses when calling it. The result of a function call is saved in a variable for other use in your code. This error can be detected by logging variable values to the console and seeing that one is set to a function reference, instead of the expected value the function returns.