---
aliases:
tags: study
---
[[JS Basic Data Structures]]
# JS Data Structures - Create Complex Multi-Dimensional Arrays
One of the most powerful features when thinking of arrays as data structures, is that arrays can contain, or even be entirely comprised of other arrays.
Arrays can contain an infinite depth of arrays that can contain other arrays, each with their own arbitrary levels of depth.
An array can quickly become a very complex data structure, known as *multi-dimensional* or *nested arrays*.

Example:

```js
let nestedArray = [
	['deep'], // 2 levels
	[
		['deeper'], ['deeper'] // 3 levels
	],
	[
		[
			['deepest'], ['deepest'] // 4 levels
		],
		[
			[
				['deepest-est?'] // 5 levels
			]
		]
	]
];
```

While this example may seem convoluted, this level of complexity is not unusual when dealing with large amounts of data. However we can still access the deepest levels of an array this complex with bracket notation:

```js
console.log(nestedArray[2][1][0][0][0]); // 'deepest-est?'
```

Now that we know where that piece of data is we can reset it if we need to:

```js
nestedArray[2][1][0][0][0] = 'deeper still';
```

Exercise: we have defined a variable `myNestedArray` set equal to an array. Modify `myNestedArray` using any combination of strings, numbers and booleans for data elements, so that it has exactly five levels of depth. Somewhere on the third level include the string `deep`, on the fourth level. include the string `deeper` and on the fifth level include the string `deepest`.

```js
let myNestedArray = [
	[
		'unshift',
		false,
		1, 2, 3,
		'complex',
		'nested',
		[
			'loop',
			'shift',
			6, 7, 1000,
			'method'
		],
		[
			'concat',
			false,
			true,
			'spread',
			'array',
			'deep',
			[
				'mutate'
				1327.98,
				'splice',
				'slice',
				'push',
				'deeper'.
				[
					'iterate',
					1.3849, 7,
					'8.4876',
					'arbitrary',
					'depth',
					'deepest'
				]
			]
		]
	]
];
```