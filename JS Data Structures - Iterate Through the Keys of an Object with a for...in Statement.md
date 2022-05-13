---
aliases: for...in
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Iterate Through the Keys of an Object with a for...in Statement
Sometimes you may need to iterate through all the keys within an object. This requires a specific syntax in JavaScript called a `for...in` statement:

```js
for (let user in users) {
	console.log(user);
}
```

This logs all the users - each value on its own line.

In this statement, we defined a variable `user` and this variable was reset during each iteration to each of the object's keys as the statements looped through the object, resulting in each user's name being printed to the console.

>[!NOTE]
>Objects do not maintain an ordering to stored keys like arrays do. A key's position on an object, or the relative order in which it appears, is irrelevant when referencing or accessing that key.

Exercise: we've defined a function `countOnline` which accepts one argument (a users object). Use a `for...in` statement within this function to loop through the users object passed into the function and return the number of users whose `online` property is set to `true`.

```js
const users = {
	Alan: {
		online: false;
	},
	Jeff: {
		online: true;
	},
	Sarah: {
		online: false;
	}
}

function countOnline(usersObj) {
	let result = 0;

	for (let user in usersObj) {
		if (usersObj[users].online === true) {
			result++;
		}
	}
	return result;
}

console.log(countOnline(users));
```