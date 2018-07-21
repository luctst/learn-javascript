---
id: hoisting
title: Hoisting in javascript
sidebar_label: Hoisting
---
>*Hoisting in javascript was build like a way to think how the execution context will work when the page is loaded.*

## Functions
```js
calculateAge(22);

calculateAge(age) {  
  return 2018 - age;
};

var retirement = (year) => {
    return 2018 - (2018 - year);
}

retirement(1995);
```
1. You can hoist functions because the computer store in memory when the page is loaded the functions you created, so you can call functions even before you create them.
2. Functions expressions is when you store a function in a variable in this case hoisting doesn't work you can't call an function expression before created her.

## Variables
```js
console.log(age);
let age = 23;
```
1. In this example the result will be `undefined` variable can't be hoist before you create them.

## Current errors
This is a list of the main errors that you can meet when you use hoisting:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.