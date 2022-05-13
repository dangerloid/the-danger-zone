---
aliases:
tags: study
---
[[JS Regular Expressions]]
# JS Regex - Match Characters that Occur Zero or More Times
There's also an option that matches characters that occur zero or more times. You use the asterisk for that.

```js
let soccerWord = "gooooooooal!";
let gPhrase = "gut feeling";
let oPhrase = "over the moon";
let goRegex = /go*/;
soccerWord.match(goRegex); // returns goooooooo
gPhrase.match(goRegex); // g
oPhrase.match(goRegex); // returns null
```

Exercise: create a regex `chewieRegex` that uses the asterisk to match an uppercase `A` followed by zero or more lowercase `a`s. No need for flags or character classes.

```js
let chewieQuote = "Aaaaaaaaaaaaaaaarrrgh!";
let chewieRegex = /Aa*/;
let result = chewieQuote.match(chewieRegex);
```