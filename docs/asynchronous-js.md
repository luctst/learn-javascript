---
id: asyncJs
title: What is asynchronous javascript
sidebar_label: Understand async js
---
>*Asynchronous javascript is code who's running in the background while our main code is still executing, this kind of code is really helpful when you want request data from a server for example.*

## Asynchronous example
```js
const second = () => {
    setTimeout( () => {
        console.log("The end");
    }, 2000 );
};

const first = () => {
    console.log("Hey there !");
    second();
    console.log("It's ok !");
};

first();
```
1. In this example we create two functions and the `second` will be run asynchronously because of the `setTimeout` function.
2. In the console the result will be first `Hey there` then `It's ok` and finally after two seconds `The end`.

## Current errors
This is a list of the main errors that you can meet:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.