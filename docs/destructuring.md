---
id: destructuring
title: ES6 destructuring
sidebar_label: ES6 destructuring
---
>*Destructuring is really helpful when you want extract values from an object or array.*

## Destructuring
```js
const [name6, age6] = ['mark',25];
return name6; // mark
return age6; // 25

const obj6 = {
  firstName: 'john',
  secondName: 'trulol'
} 
const {firstName,secondName} = obj6;
return firstName; // john
return secondName; // trulol

const {firstName: a, secondName: b} = obj6;
return a; // john
return b; // trulo
```
1. There are many possibilities of destructuring, for an array start to declare your const, let then open `[]` which indicates that you extract values from an array, after that you just need to declare the new name of your values, finally use the `=` and declare your array where the values will be extracts.
2. For object there are two ways of using destructuring, the first one is like array but instead of using `[]` you have to use `{}` and write the exact same properties, and the second one is a little bit different because you can create new variables simply add `propertiesObject: nameOfYourVariable` and that's it you create a new variable with the value of the property of the object.

## Current errors
This is a list of the main errors that you can meet with destructuring syntax:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.
