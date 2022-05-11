---
aliases:
tags: study
---
[[JavaScript]]
# JS Regex - Restrict Possible Usernames
You need to check usernames in a database. Here are some simple rules that users have to follow when creating an username:
1. Usernames can only use alpha-numeric characters
2. The only numbers in the username have to be at the end. There can be zero or more of them at the end. Username cannot start with a number.
3. Username letters can be lowercase and uppercase.
4. Usernames have to be at least two characters long. A two character username can only use alphabet letters as characters.

Exercise: change the regex `userCheck` to fit the constraints listed above.

```js
let username = "JackOfAllTrades";
let userCheck = /^[a-z][a-z]+\d*$|^[a-z]\d\d+$/i;
let result = userCheck.test(username);
```

Explanation:
- `^`: start of input
- `[a-z]`: first character is letter
- `[a-z]+`: following characters are letters
- `\d*$`: input ends with 0 or more digits
- `|`: or
- `^[a-z]`: first character is letter
- `\d\d+`: following characters are 2 or more digits
- `$`: end of input