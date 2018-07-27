---
id: es6ThisKeyword
title: ES6 this keyword
sidebar_label: ES6 this keyword
---
>*WIth ES6 the this keyword also change at last not the this keyword himself but when use with arrow function let's see that.*

## This keyword
```js
const box6 =  {
  color: 'yellow',
  position: 2,
  lexicalThis: function() {
    return this.color; // yellow
    () => this.position; // 2 !!!
  }
}
```
1. In es5 to access with `this` to a property in a regular function you have to call, `bind` `this` for that works.
2. Unlike a regular function, an arrow function does not bind `this`, instead `this` is bound lexycally.
3. In our example we create an object: `box6` we give two properties and one method and like our first example in our method we can use `this` to access properties of our current object, but this time instead of create an anonymous function with es5 we create an arrow function and because `this` is bound lexically you can use it like you did before and it's works.

## Current errors
This is a list of the main errors that you can meet:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.
