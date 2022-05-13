---
aliases:
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Add Key-Value Pairs to JavaScript Objects
At their most basic, objects are just collections of key-value pairs.

Example:

```js
const tekkenCharacter = {
	player: 'Hwoarang',
	fightingStyle: 'Tae Kwon Doe',
	human: true
};
```

The above code defines a character from Tekken as an object. It has three properties. If you want to add another property, you can do through dot notation:

```js
tekkenCharacter.origin = 'South Korea';
```

You can also add properties through bracket notation:

```js
tekkenCharacter['hair color'] = 'dyed orange';
```

This is requires when the key has spaces in it or if you want to use a variable to name the property. In the above example, the property is enclosed in quotes to denote it as a string and will be added as shown. Without quotes it will be evaluated as a variable and the name of the property will be whatever the value the variable is:

```js
const eyes = 'eye color';

tekkenCharacter[eyes] = 'brown';
```

After adding all the examples the object will look like this:

```js
{
	player: 'Hwoarang',
	fightingStyle: 'Tae Kwon Doe',
	human: true,
	origin: 'South Korea',
	'hair color': 'dyed orange',
	'eye color': 'brown'
};
```

Exercise: a `foods` object has been created with three entries. Using the syntax of your choice, add three more entries to it: `bananas` with a value of `13`, `grapes` with a value of `35`, and `strawberries` with a value of `27`.

```js
let foods = {
	apples: 25,
	oranges: 32,
	plums: 28
}

foods.bananas = 13;
foods.grapes = 35;
foods.strawberries = 27;

console.log(foods);
```