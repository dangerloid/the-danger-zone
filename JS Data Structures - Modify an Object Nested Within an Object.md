---
aliases:
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Modify an Object Nested Within an Object
Object properties can be nested to an arbitrary depth and their values can be any type of data supported by JavaScript, including arrays and other objects.

```js
let nestedObject = {
	id: 28802695164,
	date: 'December 31, 2016',
	data: {
		totalUsers: 99,
		online: 80,
		onlineStatus: {
			active: 67,
			away: 13,
			busy: 8
		}
	}
};
```

`nestedObject` has three properties: `id`, `date` and `data`. While structures can quickly become complex, we can still use the same notations to access the information we need. To assign the value 10 to the `busy` property of the nested `onlineStatus` object, we use dot notation to reference the property:

```js
nestedObject.data.onlineStatus.busy = 10;
```

Exercise: here we've defined an object `userActivity` which includes another object nested within it. Set the value of the `online` key to `45`.

```js
let userActivity = {
	id: 23894201352;
	date: 'January 1, 2017',
	data: {
		totalUsers: 51,
		online: 42
	}
};

userActivity.data.online = 45;
```