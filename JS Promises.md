---
aliases: try, catch, Promise
tags: study
---
[[JavaScript]]
# JS Promises
A promise in JavaScript is used to make a promise to do something, usually asynchronously. When the task completes, you either fulfill your promise or fail to do so.

## create a javascript promise
`Promise` is a constructor function, so you need to use the `new` keyword to create one. It takes a function as its argument with two parameters - `resolve` and `reject`. These are methods used to determine the outcome of the promise.

```js
const myPromise = new Promise((resolve, reject) => {

});
```

Exercise: create a new promise called `makeServerRequest`. Pass in a function with `resolve` and `reject` parameters to the constructor.

```js
const makeServerRequest = new Promise((resolve, reject) =>{

})
```

## complete a promise with resolve and reject
A promise has three states: `pending`, `fulfilled`, `rejected`.
The promise you created before is forever stuck in the `pending` state because you did not add a way to complete the promise.
The `resolve` and `reject` parameters given to the promise argument are used to do this. `resolve` is for when you want the promise to succeed, `reject` is for when you want it to fail.

Syntax:

```js
const myPromise = new Promise((resolve, reject) => {
	if(condition) {
		resolve("Promise was fulfilled");
	} else {
		reject("Promise was rejected");
	}
});
```

The above example uses strings, but the argument can be anything.

Exercise: make the promise handle success and failure. If `responseFromServer` is true, call the `resolve` method to successfully complete the promise. Pass `resolve` a string with the value `We got the data`. If `responseFromServer` is false, use the `reject` method instead and pass it the string `Data not received`.

```js
const makeServerRequest = new Promise((resolve, reject) => {
	let responseFromServer;
	
	if(responseFromServer) {
		resolve('We got the data');
	} else {
		reject('Data not received');
	}
});
```

## handle a fulfilled promise with then
Promises are most useful when you have a process that takes an unknown amount of time in your code (i.e. asynchronous), often a server request.
When you make a server request it takes some amount of time and after it completes you want to do something with the response. This can be done with the `then` method. `then` is executed immediately after your promise is fulfilled with `resolve`.

```js
myPromise.then(result => {

});
```

`result` comes from the argument given to the `resolve` method.

Exercise: add the `then` method to your promise. Use `result` as the parameter of its callback function and log the `result` to the console.

```js
const makeServerRequest = new Promise((resolve, reject) => {
	let responseFromServer = true;
	// set to true to represent a successful response from server

	if (responseFromServer) {
		resolve('We got the data');
	} else {
		reject('Data not received');
	}
	
	makeServerRequest.then(result => {
		console.log(result);
	})
});
```

## handle a rejected promise with catch
`catch` is the method used when your promise has been rejected. It's executed immediately after rejection.

Syntax:

```js
myPromise.catch(error => {

});
```

`error` is the argument passed in the `reject` method.

Exercise: add the `catch` method to your promise. Use `error` as the parameter of its callback function and log `error` to the console.

```js
const makeServerRequest = new Promise((resolve, reject) => {
	let responseFromServer = false;
	// set to false to represent a failed response from server

	if (responseFromServer) {
		resolve('We got the data');
	} else {
		reject('Data not received');
	}
	
	makeServerRequest.then(result => {
		console.log(result);
	})
	makeServerRequest.catch(error => {
		console.log(error);
	})
});
```