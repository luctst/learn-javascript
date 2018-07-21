---
id: letConst
title: Variables in ES6
sidebar_label: ES6 variables
---
>*ES6 include a new kinds of variables let and const.*

## Let
```js
let nom = 'lucas';
return nom; // lucas
nom = 'thomas';
return nom; // thomas

function driverlicence(passed) {
  if(passed) {
    let name = 'lucas'; // let and const create a block scop
    const age = 1995;
    return '${name} can now drive, he was born in ${age}'; // lucas can now drive, he was born in 1995
  }
  return '${name} can now drive, he\'s was born in ${age}'; // Error !!!!
}

let i = 23;

for(let i = 0; i < 5; i++) {
  return i; // 0,1,2,3,4
}

return i; // 23
```
1. With es6 you can declares variables with two new terms let, const.
2. One specific thing about `let` and `const` is the creation of block-scoped as you know in javascript a scoped is created only with functions but when you use `let` and `const` a scope is created in an if / else statements, a for loop etc.. as you can see in the example above.

## Const
```js
const age = 22;
return age; // 22
age = 25;
return age; // Error !!!
```
1. A `const` variable works exactly the same than `let` except that you can't change the value of a `const` variable.

## Current errors
This is a list of the main errors that you can meet when you use class with ES6 syntax:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.