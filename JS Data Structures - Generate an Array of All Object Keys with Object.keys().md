---
aliases: Object.keys()
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Generate an Array of All Object Keys with Object.keys()
We can generate an array which contains all the keys stores in an object using the `Object.keys()` method and passing in an object as the argument. This will return an array with strings representing each property.

Exercise: finish writing the `getArrayOfUsers` function so that it returns an array containing all the properties in the object it receives as an argument.

```js
let users = {
	Alan: {
		age: 27,
		online: false
	},
	Jeff: {
		age: 32,
		online: true
	},
	Sarah: {
		age: 48,
		online: false
	},
	Ryan: {
		age: 19,
		online: true
	}
};

function getArrayOfUsers(obj) {
	return Object.keys(obj);
}

console.log(getArrayOfUsers(users));
```