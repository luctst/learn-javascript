---
id: array
title: Array
sidebar_label: Array
---
>*An array in programmation is list or a collection of datas(primitives or objects).They are very often use for store many values in one variable, This is compared to a variable that can only store one value. There are two ways for create arrays.*

## First syntaxes
The first method is the most used and the one that we will use everytime
```js
let names = [
  'janes',
  'lucas',
  'john',
];
```
1. First create a variable and give her a name.
2. Then after the equal sign use `[]` to indicate you want a new array.
3. After that you can add everything that you want but don't forget to separate the data with a `,`.

## Second syntaxes
```js
var score = new Array(
  1,
  2,
  3,
  4
);
```
1. Here we used the same process than above but this time used the `new Array()` function to declare a new array, this syntaxe is less simple than the one before you this is why she is less used.
2. Notice that for the last element you can avoid the `,` you will not have an error.

## Current errors
This is a list of the main errors that you can meet when you use array:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.