---
id: promise
title: From callback hell to promises
sidebar_label: callback hell to promise
---
>*Promise in javascript are objects who are used to treat asynchronous code. A promise represent a value who can be available now, in the future or never.*

## How works a promise
A promise can have different states:

### Pending
The pending states means that the `Promise` simply is waiting for a certain event.

### Resolved or not
After that a certain event happened the `Promise` can now be either `resolved` or `reject` depending on the result of our callback function inside our `Promise`.

### Consume the promise
From now our `Promise` should return a result whether it is positive or negative we have a data in result, so we can access this result outside of our `Promise` with some new keywords that we will see.

## Promise in demo
Let's see with examples how you can create `Promise`.

### Create your promise
```js
const getId = new Promise( (resolve, reject) => {
    setTimeout( () => {
        resolve( [523, 883, 432, 974] );
    }, 1500 );
} );
```
1. To create `Promise` we can simply create an object by using the class `Promise`, remember that a `Promise` is simply an object with methods and properties.
2. Immediately after created your new object you have to pass a callback function with two arguments which will the result of your `Promise` remember your `Promise` can be either resolved or reject the result will be in this parameters.
3. From now the structure of your `Promise` is created you can now add some asynchronous code inside your `Promise`, for example the `setTimeout` function.
4. To say that a `Promise` is successful or not we use our parameters which are by the way functions, the first one must be called when your `Promise` is successful, the second when she's not successful. In our example when we're gonna called our `getId Promise` we know that in every case the `setTimeout` function will be executed so the `Promise` will be successful.
5. In our example our code is really simple but in most cases `Promise` are used to received data from server or AJAX requests etc.. So the `reject` parameter can be used to check if any errors happened during the process.

### Retrieve the result of your promise
```js
const getId = new Promise( (resolve, reject) => {
    setTimeout( () => {
        resolve( [523, 883, 432, 974] );
    }, 1500 );
} );

getId
.then( id => {
    console.log( id ); // [523, 883, 432, 974]
} )
.catch( error => {
    console.log(error);
} );
```
1. In function of the result of your `Promise` to retrieve the result of this one you have to use the `then` or `catch` function, The first one will be used if the result is resolved and the second if it's not.
2. Once again in each case you have to use callback function with argument that will be the result value of your `Promise`,  so our `then` method will return our array which is inside of our `resolve` function.
3. We also use the `catch` method in case of our `Promise` return a `reject` result but in this case this function will never be called because we have a `resolve` function inside our `Promise` but just to show that you can write your code like this and it will be correct.
4. As you can see our code is more clear and organize it's more simple to understand, of curse you can add as many as you want `Promise` to do some asynchronous code.
 
## Summary
1. A `Promise` is an object who keep track about a certain event who has already happen or not.
2. The `Promise` determine what happens when a certain event happened.
3. A `Promise` implement the concept of a future value that we're expecting.