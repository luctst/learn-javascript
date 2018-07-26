---
id: operator
title: Basic operator
sidebar_label: Basic operator
---
>*Javascript use operator to assign value let's see some basics operators.*

## Math operators
```js
let year = 2018;
let age = 23;

return year - age; // 1995
return year + age; // 2041;
return year / age; // 87.7;
```
1. You can use the math operator to do some calculations in your code.
2. For division you have to use this `/` syntax.

## Logical operators
```js
let year = 2018;
let age = 23;
let ageTimmy = 20;

return age > ageTimmy; // true
```
1. The logical operators are used to compare if  a value is greater or not than another one.
2. You can also use the `=` after your logical operator to check if the value is equal.

## The equals operator
```js
let year = 2018;
let age = 23;
let ageTimmy = 20;
let age2 = "23";

if ( year == age) {
    return true;
}

let valueAndType = age === age2; // false
```
1. The first equal operator that we will use a lot of time is the `=` who simply give a value.
2. The second equal operator is used to check if a value is equal to another value with this `==` syntax.
3. Finally the third equal operator is used to check if the value and the data type of our values are the same with this syntax `===`.

## Current errors
This is a list of the main errors that you can meet when you operators:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.