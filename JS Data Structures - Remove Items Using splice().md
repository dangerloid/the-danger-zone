---
aliases:
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Remove Items Using splice()
If we want to remove an item somewhere from the middle of an array, or remove more elements at once, we can use the `splice()` method.

`splice()` can take up 3 parameters but we'll focus on the first two.
The first two parameters of `splice()` are integers which represent indexes of items in the array that `splice()` is being called upon.
`splice()`'s first parameter represents the index on the array from which to begin removing elements, while the second parameter indicates the number of elements to delete.

Example:

```js
let array = ['today', 'was', 'not', 'so', 'great'];

array.splice(2, 2); // removed 'not' and 'so'
```

`splice()` not only modifies the array it's being called on, but it also returns a new array containing the value of the removed elements.

```js
let array = ['I', 'am', 'feeling', 'really', 'happy'];

let newArray = array.splice(3, 2); // value is ['really', 'happy']
```

Exercise: we've initialized an array `arr`. Use `splice()` to remove elements from `arr` so that it only contains the sum to the value of 10.

```js
const arr = [2, 4, 5, 1, 7, 5, 2, 1];

arr.splice(0, 2);
arr.splice(1, 2);
arr.splice(2, 2);

console.log(arr);
```
