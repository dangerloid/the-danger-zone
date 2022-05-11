---
aliases:
tags: study
---
[[JavaScript]]
# JS Debugging - Catch Off By One Errors When Using Indexing
Off by one errors (OBOE) crop up when you're trying to target a specific index of a string or array, or when looping over the indices of them.
JavaScript indexing always starts at zero, which means the last index is always one less than the length of the item.

When you use string or array methods that take index ranges as arguments, it helps to read the documentation and understand if they are inclusive.