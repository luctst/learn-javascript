---
id: es6Async
title: From promise to ES6 async
sidebar_label: Promise to ES6 async
---
>*We saw that there are many ways to do asynchronous code in javascript from callback function to promise, but now with ES6 there is a new way to do asynchronous code with the (async, await) keywords. This ES6 syntax must be used with Promise so this is a not a new way to produce async code but a better way to consume Promise by avoid all this `then` and `catch` method.*

## Async function
```js
const getId = new Promise( (resolve, reject) => {
    setTimeout( () => {
        resolve( [100, 200, 300, 400] );
    }, 1500 );
} );

const getIdAw = async () => {
    const Id = await getId;
    console.log(Id);
};

getIdAw();
```
1. Like we said `async` functions is a new way to consume `Promise`.
2. You can create an `async` function simply by using the `async` keywords in front of your function, this will tell to the javascript engine this function will run in background.
3. Remember that we said that inside an `async` function we can access the result of our `Promise` function (resolve, reject), in order to do that you have to use the `await` keywords and called your `Promise`.
4. So in summary we can tell that the `getIdAw` function is an asynchronous function who runs in the background of our code and wait for `Promise` to be resolved or not.
5. You can use inside your `async` function ordinary code which means without `await` but the result will always be convert to a `Promise`.

## Current errors
This is a list of the main errors that you can meet:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.