---
aliases:
tags: study
---
[[JavaScript]]
# JS Import and Export
## create a module script
JavaScript started with a small role to play on an otherwise mostly [[HTML]] web.
Today, most websites are built almost entirely with JavaScript.
In order to make JavaScript more modular, clean and maintainable, ES6 introduced a way to easily share code among JS files.
This involves exporting parts of a file for use in one or more other files and importing the parts you need.
To do this, you need to create a script in your HTML document with a type of `module`.

```html
<script type="module" src="filename.js"></script>
```

A script that uses this `module` type can now use the `import` and `export` features.

## use export to share a code block
Scenario: you have a file called `math_functions.js` that contains several functions related to mathematical operations. One of them is stored in a variable called `add` that takes two numbers and returns their sum. You want to use this function in several different JavaScript files. To do this you'll need to `export` it.

```js
export const add = (x, y) => {
	return x + y;
}
```

You can also do this:

```js
const add = (x, y) => {
	return x + y;
}

export {add};
```

When you export a variable or function, you can import it in another file and use it without rewriting the code. You can export multiple things by repeating the first example for each thing you want to export, or by placing them all in the export statement of the second example:

```js
export {add, subtract};
```

Exercise: there are two string-related functions in the editor. Export both of them using the method of your choice.

```js
const uppercaseString = (string) => {
	return string.toUpperCase();
}

const lowercaseString = (string) => {
	return string.toLowerCase();
}

export {uppercaseString, lowercaseString}
```

## reuse javascript code using import
`import` allows you to choose which parts of a file or module to load.

Using the example above:

```js
import {add} from './math_functions.js';
```

Here `import` will find `add` in `math_functions.js`, import just that function for you to use and ignore the rest.

You can import more than one item from the file buy adding them in the `import` statement:

```js
import {add, subtract} from './math_functions.js';
```

Exercise: add the appropriate `import` statement that will allow the current file to use the `uppercaseString` and `lowercaseString` functions. These functions are in a file called `string_functions.js`.

```js
import {uppercaseString, lowercaseString} from './string_functions.js';

uppercaseString("hello");
lowercaseString("WORLD!");
```

## understand the difference between import and require
In the past people would use the `require` function to import functions and code from another file.

## use * to import everything from a file
Scenario: you have a file and you want to import all of its contents into the current file. This can be done with the `import * as` syntax.

Example:

```js
import * as myMathModule from './math_functions.js';
```

The above `import` statement will create an object called `myMathModule`.
The object will contain all of the exports from `math_functions.js` so you can access the functions like you would any object property:

```js
myMathModule.add(2,3);
myMathModule.subtract(5,3);
```

Exercise: the code in this file requires the contents of the file: `string_functions.js`, that is in the same directory as the current file. Use the `import * as` syntax to import everything form the file into an object called `stringFunctions`.

```js
import * as stringFunctions from './string_functions.js';

stringFunctions.uppercaseString("hello");
stringFunctions.lowercaseString("WORLD!");
```

## create an export fallback with export default
There's another `export` syntax, known as *export default*. You will use this syntax if only one value is being exported from a file. It's also used to create a fallback value for a file or module.

```js
export default function add (x, y) {
	return x + y;
} // named function

export default function (x, y) {
	return x + y;
} // anonymous function
```

Since `export default` is used to declare a fallback value for a module or file, you can only have one value be a default export per module or file. You cannot use this with variable keywords.

Exercise: the following function should be the fallback value for the module. Add the necessary code.

```js
export default function subtract(x, y) {
	return x - y;
}
```

## import a default export
To import a default export, you need to use a different `import` syntax:

```js
import add from './math_functions.js';
```

The difference being that the imported value is not surrounded by curly braces. `add` is simply a variable name for whatever the default export is.

Exercise: in the following code, import the default export from `math_functions.js`, found in the same directory as this file. Give the import name `subtract`.

```js
import subtract from './math_functions.js';

subtract(7,4);
```