---
aliases:
tags: study
---
[[JS Data Types]]
# Object

An object can store different key values pairs.

## build javascript objects
Objects are similar to arrays, except instead of using indexes to access and modify their data, you access them through `properties`.

Objects are useful for storing data.

Example for syntax:

```js
const myDog = {
	"name": "Pluto",
	"legs" = 4,
	"tails" = 1,
	"friends": ["Mickey", "Donald", "Goofy"]
};
```

Key names are strings, but they can be written as keywords (without quotes) and they will still be read as strings.
Values accept any data type.
When you're done with a key value pair, you end it with a comma and go to the next line. For the last key value pair, you don't need a comma.

## accessing object properties with dot notation
You can access object properties with both dot notation and bracket notation.

Dot notation is what you use when you know the name of the property you're trying to access. `myObj.prop1`

Example:

```js
const testObj = {
	"hat": "ballcap",
	"shirt": "jersey",
	"shoes": "cleats"
};

const hatValue = testObj.hat;
const shirtValue = testObj.shirt;
```

## accessing object properties with bracket notation
You can use bracket notation anytime, but if the property of the object you're trying to access has a space in its name, it's required.

```js
const testObj = {
	"an entree": "hamburger",
	"my side": "veggies",
	"the drink": "water"
};

const entreeValue = testObj["an entree"];
const drinkValue = testObj["the drink"];
```

## accessing object properties with variables
Bracket notation can be used to access object properties stored in the value of a variable. This can be useful for iterating through an object's properties.

You can use this when the property's name is collected dynamically during the program execution.

```js
const someObj = {
	propName = "John"
};

function propPrefix(str) {
	const s = "prop";
	return s + str;
}

const someProp = propPrefix("Name");
console.log(someObj[someProp]);
```

`someProp` would have a value of the string `propName` and the string `John` will be displayed in the console.

Exercise: set the `playerNumber` to `16`. Then use the variable to look up the player's name and assign it to `player`.

```js
const testObj = {
	12: "Namath",
	16: "Montana",
	19: "Unitas"
};

const playerNumber = 16;
const player = testObj[playerNumber];
```

## updating object properties
After creating a JavaScript object, you can update its properties at any time just like you would do with variables.

```js
const myDog = {
	"name": "Coder",
	"legs": 4,
	"tails": 1,
	"friends": ["freeCodeCamp Campers"]
};

myDog.name = "Happy Coder";
// myDog["name"] = "Happy Coder";
```

## add new properties to a javascript object
Adding properties to object is the same as updating them.

```js
const myDog = {
	"name": "Coder",
	"legs": 4,
	"tails": 1,
	"friends": ["freeCodeCamp Campers"]
};

myDog.bark = "woof";
```

## delete properties from a javascript object
We can delete a property with the keyword `delete`.

```js
const myDog = {
	"name": "Coder",
	"legs": 4,
	"tails": 1,
	"friends": ["freeCodeCamp Campers"]
};

delete myDog.tails;
```

## using objects for lookups
Object can be thought of as a key/value storage.
If you have tabular data, you can use an object to lookup values rather than a `switch` statement or an `if`/ `else` chain.

In this exercise, I had to convert a switch statement into an object.

```js
function phoneticLookup(val) {
	let result = "";

	var lookup = {
		alpha: "Adams",
		bravo: "Boston",
		charlie: "Chicago",
		delta: "Denver",
		echo: "Easy",
		foxtrot: "Frank"
	};
	result = lookup[val];
}

phoneticLookup("charlie"); // returns "Chicago"
```

## testing objects for properties
Sometimes it is useful to check if the property of a given object exists or not. We can use the `.hasOwnProperty()` [[JS Methods|method]] to determine if that object has the given property name. It returns a boolean value.

```js
function checkObj(obj, checkProp) {
	if obj.hasOwnProperty(checkProp) {
		return obj[checkProp]
	} else {
		return "Not Found"
	}
}
```

## manipulating complex objects
Sometimes you may want to store data in a flexible data structure. A JavaScript object is one way to do so. They allow for arbitrary combinations of any data type.

Example:

```js
const ourMusic = [
	{
		"artist": "Daft Punk",
		"title": "Homework",
		"release_year": 1997,
		"formats": [
			"CD",
			"Cassette",
			"LP"
		],
		"gold": true
	}
];
```

This is an array within an object within an array. It displays metadata about Daft Punk's Homework. If you want to add more albums to this array, you can do this by adding records to the top level array.
Objects hold data in a property, which has a key/value format.
The code inside the `ourMusic` constant is pure JSON.

Exercise: add another album to the `myMusic` array. Needs to include `artist`, `title` (strings), `release_year` (number) and `formats` (array with strings).

```js
const myMusic = [
	{
		"artist": "Billy Joel",
		"title": "Piano Man",
		"release_year": 1973,
		"formats": [
			"CD",
			"8T",
			"LP"
		],
		"gold": true
	},
	{
		"artist": "Radiohead",
		"title": "OK Computer",
		"release_year": 1997,
		"formats": [
			"CD",
			"Cassette",
			"LP"
		],
		"gold": true
	}
];
```

## accessing nested objects
The sub-properties of objects can be accessed by chaining together the dot or bracket notation.

Exercise: access the `myStorage` object and assign the content of `glove box` to `gloveBoxContents`.

```js
const myStorage = {
	"car": {
		"inside": {
			"glove box": "maps",
			"passenger seat": "crumbs"
		},
		"outside": {
			"trunk": "jack"
		}
	}
};

const gloveBoxContents = myStorage.car.inside["glove box"];
```

## accessing nested arrays
Objects can contain both nested objects and arrays. Array bracket notation can be chained to access nested arrays.

Example: we have an array of animals.

```js
const ourPets = [
	{
		animalType: "cat",
		names: [
			"Meowzer",
			"Fluffy",
			"Kit-Cat"
		]
	},
	{
		animalType: "dog",
		names: [
			"Spot",
			"Bowser",
			"Frankie"
		]
	}
];

ourPets[0].names[1]; // Fluffy
ourPets[1].names[0]; // Spot
```

Exercise: using dot and bracket notation, set the variable `secondTree` to the second item in the `trees` list from the `myPlants` object.

```js
const myPlants = [
	{
		type: "flowers",
		list: [
			"rose",
			"tulip",
			"dandelion"
		]
	},
	{
		type: "trees",
		list: [
			"fir",
			"pine",
			"birch"
		]
	}
];

const secondTree = myPlants[1].list[1]; // pine
```

## record collection (fcc exercise)
I have an object literal representing part of an album collection. Each album has a unique id number as its key and multiple properties. Not all albums have complete information.

The function `updateRecords` takes `records`, `id`, `prop` (can be `artist` or `tracks`) and `value`.
Complete the function following these instructions:
- the function must always return the entire object;
- if `prop` isn't `tracks` and `value` isn't an empty string, update or set that album's prop to value;
- if `prop` is `tracks` but the album doesn't have a `tracks` property, create an empty array and add `value` to it;
- if `prop` is `tracks` and `value` isn't an empty string, add `value` to the end of the album's existing `tracks` array;
- if `value` is an empty string, delete the given `prop` property from the album.

```js
const recordCollection = { // don't touch the object
	2548: {
		albumTitle: "Slippery When Wet",
		artist: "Bon Jovi",
		tracks: ["Let It Rock", "You Give Love A Bad Name"]
	},
	2468: {
		albumTitle: "1999",
		artist: "Prince",
		tracks: ["1999", "Little Red Corvette"]
	},
	1245: {
		artist: "Robert Palmer",
		tracks: []
	},
	5439: {
		albumTitle: "ABBA Gold"
	}
};

function updateRecords(records, id, prop, value) {

	if (value === "") {
		delete records[id][prop];
	} else if (prop === "tracks") {
		records[id][prop] = records[id][prop] || [];
		records[id][prop].push(value);
	} else {
		records[id][prop] = value;
	}

	return records;
}

updateRecords(recordCollection, 5439, "artist", "ABBA")
```

## prevent object mutation
`const` declaration alone doesn't protect data from mutation. To ensure your data doesn't change, JavaScript (as of ES6's release in 2015) provides the `Object.freeze` function to prevent data mutation.

Any attempt at changing the object will be rejected.

Exercise: use `Object.freeze` to prevent mathematical constants from changing.

```JS
function freezeObj() {
	const MATH_CONSTANTS = {
		PI: 3.14
	};
	Object.freeze(MATH_CONSTANTS);
	try {
		MATH_CONSTANTS.PI = 99; 
	} catch(ex) {
		console.log(ex);
	} return MATH_CONSTANTS.PI;
} const PI = freezeObj()
```

## use destructuring assignment to extract values from objects
Destructuring assignments is special syntax introduced in ES6 for assigning values taken from an object.

ES5 example code:

```js
const user = { name: 'John Doe', age: 34 }

const name = user.name;
const age = user.age; // i hate that!!!!!!!!
```

`name` would have a value of the string `John Doe` and `age` would have the number 34.

Here's the same but in ES6:

```js
const { name, age } = user;
```

Here we created two constants named `name` and `age` and assigned them to items in the object `user`.

Exercise: replace the two assignments with an equivalent destructuring assignment. It should still assign the variables `today` and `tomorrow` the values of `today` and `tomorrom` from the `HIGH_TEMPERATURES` object.

```js
const HIGH_TEMPERATURES = {
	yesterday: 75,
	today: 77,
	tomorrow: 80
};

const { today, tomorrow } = HIGH_TEMPERATURES;
```
## use destructuring assignment to assign variables from objects
Destructuring allows you to assign a new variable name when extracting values. You can do this by putting the new name after a colon when assigning the value.

Example, same object as above:

```js
const { name: userName, age: userAge } = user;
```

"Get the value of `user.name` and assign it to a variable called `userName`".

Exercise: replace the two assignments with an equivalent destructuring assignment.

```js
const HIGH_TEMPERATURES = {
	yesterday: 75,
	today: 77,
	tomorrow: 80
};

const { today: highToday, tomorrow: highTomorrow } = HIGH_TEMPERATURES;
```
## use destructuring assignment to assign variables from nested objects
You can use the same principles to destructure values form nested objects.

Similar object from before, we'll see how to extract the values of the object properties and assign them to variables with the same name:

```js
const user = {
	johnDoe: {
		age: 34,
		email: 'johnDoe@cazzimazzi.com'
	}
};

const {johnDoe: {age, email}} = user;
// OR
const {johnDoe: {age: userAge, email: userEmail}} = user;
```

Exercise: replace the two assignments with an equivalent destructuring assignment.

```js
const LOCAL_FORECAST = {
	yesterday: {low: 61, high: 75},
	today: {low: 64, high: 77},
	tomorrow: {low: 68, high: 80}
};

const {today: {low: lowToday}} = LOCAL_FORECAST;
const {today: {high: highToday}} = LOCAL_FORECAST;
```

## use destructuring to pass an object as a [[JS Functions|function]]'s parameter
In some cases, you can destructure the object in a function argument itself.

Example. This destructures the object sent into the function.

```js
const profileUpdate = (profileData) => {
	const {name, age, nationality, location} = profileData;
}
```

Can also be done in-place:

```js
const profileUpdate = ({name, age, nationality, location}) => {

}
```

When `profileData` is passed to the above function, the values are destructured from the function parameter for use withing the function.

Exercise: use destructuring assignment withing the argument to the function `half` to sent only `max` and `min` inside the function.

```js
const stats = {
	max = 56.78,
	standard_deviation: 4.34,
	median: 34.54,
	mode: 23.87,
	min: -0.75,
	average: 35.85
};

const half = ({max, min}) => {
	return (max + min) / 2.0;
} 
```

## write concise object literal declarations using object property shorthand[^1]
ES6 adds support for object literals.

Example:

```js
const getMousePosition = (x, y) => ({
	x: x,
	y: y
});
```

`getMousePosition` is a simple function that returns an object containing two properties. ES6 provides the syntactic sugar to eliminate the redundancy of having to write `x: x`.

```js
const getMousePosition = (x, y) => ({x, y});
```

Exercise: use object property shorthand with object literals to create and return an object with `name`, `age` and `gender` properties.

```js
const createPerson = (name, age, gender) => {
	return ({name, age, gender});
}
```

## use class syntax to define a constructor function
ES6 added new syntax to create objects using the `class` keyword.

>[!NOTE]
>The class syntax is just syntax, not a full-fledged class-based implementation of an object-oriented paradigm, unlike other languages like Python.

In ES5, we usually define a `constructor` function and use the `new` keyword to instantiate an object.

```js
var SpaceShuttle = function(targetPlanet) {
	this.targetPlanet = targetPlanet;
}
var zeus = new SpaceShuttle('Jupiter');
```

The `class` syntax replaces the `constructor` function creation:

```js
class SpaceShuttle {
	constructor(targetPlanet) {
		this.targetPlanet = targetPlanet;
	}
}
const zeus = new SpaceShuttle(`Jupiter`);
```

The `class` keyword declares a new function, to which a `constructor` is added. The constructor is invoked when `new` is called to create a new object.

>[!NOTE]
>UpperCamelCase should be used by convention for ES6 class names.

The `constructor` [[JS Methods|method]] is for initializing an object created with a class.

Exercise: use the `class` keyword and write a `constructor` to create the `Vegetable` class.
The `Vegetable` class allows you to create a vegetable object with a property `name` that gets passed to the `constructor`.

```js
class Vegetable {
	constructor(name) {
		this.name = name;
	}
}

const carrot = new Vegetable('carrot');
```

## use getters and setters to control access to an object
You can obtain values from an object and set the value of a property within an object.

They're called *getters* and *setters*.

Getter functions are meant to simply return the value of an object's private variable to the user without them directly accessing the private variable.

Setter functions are meant to modify the value of an object's private variable based on the value passed into the setter function.

```js
class Book {
	constructor(author) {
		this._author = author;
	}
	// getter
	get writer() {
		return this._author;
	}
	// setter
	set writer(updatedAuthor) {
		this._author = updatedAuthor;
	}
}

const novel = new Book('anonymous');
console.log(novel.writer);
novel.writer = "newAuthor";
console.log(novel.writer);
```

The console will display the strings `anonymous` and `newAuthor`.

The syntax for getters and setters doesn't look very function-like. They're important because they hide implementation details.

>[!NOTE]
>It's convention to start the name of a private variable with an underscore.

Exercise: use the `class` keyword to create a `Thermostat` class. The constructor accepts a Fahrenheit temperature.
In the class, create a `getter` to obtain the temperature in Celsius and a `setter` to set the temperature in Celsius.

```js
class Thermostat {
	constructor(temp) {
		this._temp = 5/9 * (temp - 32);
	}
	get temperature() {
		return this._temp:
	}
	set temperature(updatedTemp) {
		this._temp = updatedTemp;
	}
}

const thermos = new Thermostat(76);
let temp = thermos.temperature;
termos.temperature = 26;
temp = thermos.temperature;
```

### related notes
[[JSON]] - JavaScript Object Notation


#### footnotes
[^1]: [[JS String#create strings using template literals]]
