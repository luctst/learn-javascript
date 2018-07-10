---
id: thisKeyword
title: This keyword 
sidebar_label: The this keyword in practice
---
> *The this keyword returns the value of the context where it's called, in a regular function the this keyword points at the global object, (the window object in the browser). in a method (function in object) this points to the object that it's calling.*

## This in a regular function
```js
function calculateAge(year) {
    console.log( 2018 - year );
    console.log(this);
}
```
In this example we use this in a regular function so the value of `this` will be the window object because we call this in a **regular function**.

> **Note:** - With ES6 and arrow functions the `this` keyword will point to the actual function.

## This in an object
```js
let perso = {
    name: John,
    yearOfBirth: 1995,
    calculateAge: function () {
        console.log(this);
    }
}
```
In this example we use the this keyword in an method so it will returns the `perso` object.

## Function in a method
```js
let perso = {
    name: John,
    yearOfBirth: 1995,
    calculateAge: function () {
        console.log(this);

        function innerFunction () {
            console.log(this);
        }
        innerFunction();
    }
}
```
This time we call a regular function inside a method so the `this` keyword will return the window object because it's still a regular function.

## Current errors
This is a list of the main errors that you can meet when you use this keyword:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.