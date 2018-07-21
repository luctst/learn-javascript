---
id: eventLoop
title: Event loop in asynchronous
sidebar_label: Event loop
---
>*The event loop in javascript handle what happens behind the scenes in js when you call callback functions, DOM events etc..*

## How asynchronous works
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
1. In the execution stack we add on top the `first execution context` we now execute the code inside of this function, the first line is called so in the console you should now have `hey there` display. Then we call the `second function` we now put on top of the execution stack the `second` function.
2. We call the `setTimeout` function so we now have on the top of the execution stack the `setTimeout` function, but as you can see this function has a callback function which means she will be run asynchronously after 2s because of the second argument `2000`.
3. What happen now ? We don't execute the code directly when the function is called because she's need to run asynchronously so the function will be moved into the `Web api environment`, from now the function will be running in the background of our code and we can keep going executing the code so we can remove the `setTimeout execution context` and also the `second execution context`.
4. Back in our `first execution context` we can execute the last line of code and now our console should have `hey there it's ok`. Right now all our synchronous code was executed we can now be focus on our asynchronous code.
5. Let's say that 2s are passed so our `setTimeout` function can now be executed so she will be moved to the `message queue environment`.
6. This environment hold all the functions who's waiting to be push in the `execution stack` as soon as this one is empty, in our example our `execution stack` is empty and our `message queue` environment contains the `setTimeout` function so we can push this one in the `execution stack`.
7. Our execution stack is now on top `setTimeout` function so we can execute the code inside this one and our console should now displayed `hey there it's ok the end`.

## Current errors
This is a list of the main errors that you can meet:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.