---
aliases: .hasOwnProperty, in
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Check If an Object has a Property
If we wanted to know if an object has a specific property, we can use the `.hasOwnProperty()` method or the `in` keyword.
If we have an object `users` with a property of `Alan`, we could check for its presence in either of the following ways:

```js
users.hasOwnProperty('Alan');
'Alan' in users;
```

Exercise: finish writing the function so that it returns `true` if the object passed to it contains all four names `Alan`, `Jeff`, `Sarah` and `Ryan` and returns `false` otherwise.

```js
let users = {
	Alan: {
		age: 27,
		online: true
	},
	Jeff: {
		age: 32,
		online: true
	},
	Sarah: {
		age: 48,
		online: true
	},
	Ryan: {
		age: 19,
		online: true
	}
};

function isEveryoneHere(userObj) {
	if (userObj.hasOwnProperty('Alan') &&
		userObj.hasOwnProperty('Jeff') &&
		userObj.hasOwnProperty('Sarah') &&
		userObj.hasOwnProperty('Ryan')) {
		return true;
	}
	return false;
}

console.log(isEveryoneHere(users));
```

---

## related notes
[[JS Object#testing objects for properties|.hasOwnProperty()]]