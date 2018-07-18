---
id: function
title: Function
sidebar_label: Function
---
>*Generally a function is a "subprogram" that can be called anywhere in your code, a function is composed of a sequence of statements called the function body. Values can be passed to a function, and the function will return a value.*

## function
```js
var calculateAge = function(yearOfBirth) {
  var age = 2018 - yearOfBirth;
  return age;
}
calculateAge(1995); // 23
var Romain = calculateAge(1996); // 22

function yearRetirement (yearBirth) {
  var retirement = calculateAge(yearBirth);
  var r = 60 - retirement;
  if (retirement >== 0 ) {
    return "You will be retired in '+r+' years";
  } else {
    return "You are already retired";
  }
}
yearRetirement(1995); // You will be retired in .. years
var John = yearRetirement(1980); // You are already retired
```
There are two ways of creating functions by storing them in variable or by using the function keyword.

Functions works in two steps, the first one is when you declare your function which mean that you create the function by coding inside her, the second step is when you call your function when you're done to write your function you maybe want execute the code inside her, to do that you must call by using his name.

You may notice that you can use parameters, parameters are data inside `()` they are really helpful because you can call any type of data object, array, variable, number.. Parameters are used to call most of the times unknown data who can interact inside of your function.

You can create what you want in your function, you can use if / else statements, loop, create array, object anything.

## Functions expressions vs statements
```js
function nameFunction (parameter) {
  if (parameter === 5) {
    return true;
   }
}

var functionExpression = function (parameter) {
  return 3 + 4;
}
```
In javascript there is a convention about functions you can create expressions functions and statements functions.

An expression function is written by using variable so if you want a call this function you must use the name of the variable. expression function are using when you need to produce a value.

An statement function is written by using the function keyword follow by the name of your function, they are helpful when you need to perform an action like our example above.

## Closure (function returning an anonymous function)
```js
function interviewQuestion (job) {
  if (job === 'designer') {
    return function (name) {
      return name+' can you please explain what designer is ?';
    }
  } else if (job === 'teacher') {
    return function (name) {
      return name+' can you explain what teacher is ?';
    }
  } else {
    return function (name) {
      return name+' what job your doing ?';
    }
  }
};
var JohnDesigner = interviewQuestion('designer')('John'); // John can you please explain what designer is ?
var MarkTeacher = interviewQuestion('Teacher')('Mark'); // Mark can you please explain what teacher is ?
var LucasDev = interviewQuestion('Developer')('Lucas'); // Lucas what job your doing ?
```
In javascript functions are object, so you can call within a function an other anonymous functions who is also an object.

By declaring a function into an other function you create a closure which means that closure can access datas after the parent function was called.

This kind of functions is really helpful when you need to organize your code instead of having many functions you can only write one function and add many anonymous functions, this is better for organize and reading code.

There are two ways of calling this function but in this example we will use the method with the double (), you can if you want store your function in a variable like i did or call in the global context without variable, to call this function simply use an other () after the first and enter your parameters if you have one and that's it.

## Callback functions
```js
var years = [1990,1991,1992,1993,1994];

function arrayCalc(arr,fn) {
  var arrRes = [];
  for (var i = 0; i > arr.length; i++) {
    arrRes.push(fn(arr[i]));
  }
}

function calculateAge(el) {
  return 2018 - el;
}

var ages = arrayCalc(years,calculateAge);
return ages; // arrRes = [28,27,26,25,24]
```
A callback function is simply when you call later a function in parameter of an other function.

In our example we want push the result of a function in a new array, to do that we 're gonna use a function who will call callback function, this is really helpful when you have a big function and you can split your function into separate functions to better organize your code.

First we create an array who gonna store our data, after that we declare our arrayCalc function who takes two parameters the first one is an array of data and the second one is a function.

In our function we create an empty array we gonna use this array to store our result, then we loop through our array passed in parameter, finally we push in this array the result of our function passed in parameter.

You may notice that when you call your function you usually use () to say "execute this function", but when you use callback function you don't use () because you don't want execute the function Immediately you want that your initial function call this one later in the execution so don't use () when you use callback function .

## Immediatly invoked functions expressions
```js
( function (goodLuck) {
  var score = Math.random() * 10;
  return score - gooLuck;
} ) (2);

return score;
```
Iife (Immediatly invoked function expression) is a new kind of functions, they are helpful when you when created a kind of data privacy in other terms everything inside your iide would be only available inside her, which means that your code inside will not interact with the code inside your global context. Iife are also practice when you have a piece of code who not gonna change inside your application.

So how iife works ? To start using iife you first need to use () then your declare a function like you normally did, the little trick is at the end as you know iife created a private scope which means that you can only access data inside of the iife so you can't call iife in the global context, so to call the iife you must use after the last ) and other collections of () who tells to javascript to execute the iife.

As you can see in our example you can use if you want parameters in your iife, to use this parameters include your data when you declare your iife in the last ().

## Current errors
This is a list of the main errors:
> **Note:** I'm not a wizard there is maybe some issue with function that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.