---
id: primitiveVsObject
title: Data in primitives vs objects
sidebar_label: primitive vs object
---
>*We already saw what is primitives and object in this lesson [data type](learn-javascript/docs/dataType.html), but let's see now what is the differences between this two datas types.*

## Primitive
When you called a primitive data you actually called the value of this primitive data. Let's see with an example.
```js
let a  = 26;
let b = a;

console.log(a); // 26
console.log(b); // 26

a = 43;

console.log(a); // 46
console.log(b); // 26
```
1. In this example we create two variables `a` and `b`, first `a` is equal to `26` then `b` is equal to `a`.
2. If you return the two variables no surprise they are both equals to `26`.
3. What if now we change the value of  `a` ? Does `b` will change too ? Well the answer is no like their are both primitives and remember primitives contains the copy of the value `b` will not change.

## Object
We saw that primitives datas contain the copy of the value and their results doesn't change even if you change another variable who is equal. Objects works a little bit differently, when you create an object the computer create an unique id for this object so when an object is equal to another object they are both calling the same id.
```js
let obj1  = {
    age: 23,
    name: "lucas"
}

let obj2 = obj1;

obj1.age = 30;

console.log(obj1);
console.log(obj2);
```
1. First we create an object with two properties `name` and `age`.
2. Then we create a variable `obj2` which is an object because it's equal to `obj1`.
3. After that we change the value of `obj1.age` by 30 and return the two objects.
4. What happen now it's the two properties objects are changed, and that's because like we said datas object doesn't hold an value like primitive but an reference who is called every time this two objects.

## Current errors
This is a list of the main errors that you can meet:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.