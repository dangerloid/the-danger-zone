---
aliases: delete
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Use the delete Keyword to Remove Object Properties
Let's see the `foods` object again.
If we wanted to remove the `apples` key, we use the `delete` keyword:

```js
delete foods.apples;
```

Exercise: use the `delete` keyword to remove the `oranges`, `plums` and `strawberries` keys from the `foods` object.

```js
let foods = {
	apples: 25,
	oranges: 32,
	plums: 28,
	bananas: 13,
	grapes: 35,
	strawberries: 27
}

delete foods.oranges;
delete foods.plums;
delete foods.strawberries;

console.log(foods);
```