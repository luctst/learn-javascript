---
id: arrowFunction
title: ES6 arrow functions
sidebar_label: ES6 arrow function
---
>*With ES6 a new way of written function is available and really helpful.*

## Function arrow
```js
// Variable
const years = 1995;
const name = 'lucas';
let ages6;

// Es6
ages6 = yearOfBirth => 2018 - yearOfBirth; // One line syntax
return ages6(years); // 22

ages6 = (yearOfBirth,name) => `${name} was born in ${yearOfBirth}`; // Two or more parameters syntax
return ages6(years,name) // lucas was born in 1995

ages6 = (name,yearOfBirth) => { // Many lines syntax
  const now = new Date().getFullYear(); // 2018
  const age = now - yearOfBirth; // 22;
  return `${name} was born in ${yearOfBirth} and he's ${age}`; // lucas was born in 1995 and he's 22.
}
```
1. You can now write functions with this new syntax, first you have to store function in a variable, then the first word will be parameter(s) of your function, after that use `=>` to start declare the line(s) of your function, you will se later that you may need this `{}` but we will see later.
2. There are many possibilities in es6 functions you may have, one parameter and one line, one or more parameters and one line, and one or more parameters but many lines, let's see all examples.
3. One parameter and one line, in this example after your variable declaration write your parameter use `=>` and write your function declaration, notice that with this syntax you don't have to use `return` es6 did it for you.
4. One or more parameters and one line , for this case the syntax is the same except that you need to frame your parameters in `()`, same thing with `return`.
5. Finally one or more parameters but many lines , for this case the syntax is a little bit different of curse same principle for parameter(s) but this time if you have to declare more than one line in your function declaration you must use `{}`, and declare `return` if you want use it.

## Current errors
This is a list of the main errors that you can meet when you use arrow function:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.


