---
aliases:
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Access an Array's Contents Using Bracket Notation
The fundamental feature of any data structure is not only the ability to store data, but to be able to retrieve it on command.

When we define a simple array there are three items in it:

```js
let ourArray = ['a', 'b', 'c'];
```

In an array. each item has an index. This index doubles as the position of the item in the array and how you referencing.
It's important to note that JavaScript is *zero-indexed*, meaning that the first element of the array is at the zeroth position.
To retrieve an item from an array, we enclose its index in brackets and append it to the end of the array, or the variable it's assigned to.
This is called *bracket notation*.

Example: if we want to retrieve an item from the above array:

```js
let ourVariable = ourArray[0]; // variable has value of a
```

In addition to accessing the value associated with an index, you can also set an index to a value using the same notation:

```js
ourArray[1] = 'not b anymore'; // changed the value of the second item
```

Exercise: in order to complete this challenge, set the 2nd position of `myArray` to anything you want, besides the letter b.

```js
let myArray = ['a', 'b', 'c', 'd'];
myArray[1] = "don't b so serious";
console.log(myArray);
```