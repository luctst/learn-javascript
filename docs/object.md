---
id: object
title: Object
sidebar_label: Object
---
> Object are really useful in javascript they allow you to structure your code and better organize your application.

## Create an object
Create an object is really simple there are many methods to do that but in this courses we will use the most used:
```js
const name = {};
```
1. To create an `object` simply create a `variable`.
2. After the = open curly braces, the computer will understand that you create an object.

## Properties in object
`Object` are like `arrays` you can store many properties that you can call later to create a properties:
```js
const name = {
    firstName: "lucas",
    lastName: "Tostée",
    age: 22,
    friends: ["keke","gigi"],
    stuff: {}
}
```
1. The first thing for create a property is to give a name followed by `:`, it's important to use double point instead of = when you are in object you have to use this syntax.
2. Each properties is ending by a `,` which tell to the computer this properties is done you can switch to another one.
3. You may notice that you can stores anything that you want in properties like `string`, `number`, `array` etc.. and even other object.

### Access properties
Once you create your properties you maybe want to access it or modify etc.. ? Let's see how you can do that:
```js
const name = {
    firstName: "lucas",
    lastName: "Tostée",
    age: 22,
    friends: ["keke","gigi"],
    stuff: {}
}

return name.firstName; // Lucas
return name["age"]; // 22
return name.friends[0]; // keke
return name.lucas = "Hugo";
```
1. There are two ways of access `properties` in object, the first one and the most used is the dot notation.
2. Simply call the name of your object and use `.` followed by your properties name.
3. The second method is with `[]`.
4. Repeat the same operation than the dot notation but use `["propertiesName"]` after your object name.
5. If you want modify the content of a properties you can use = and the value that you want to modify the property.

## Methods in object
From now we saw how to stores informations in an object but what if we want create `function` inside object. Let's see how you can create `methods`:
```js
const name = {
    firstName: "lucas",
    yearBirth: 1995,
    calcAge: function () {
        return 2018 - this.yearBirth;
    }
}
```
1. A lot of new things here, so first a function in object is called a `method` and you can create a method just like properties but used the word `function` after the double points.
> **Note** - The new keyword `this` is a little bit strange for now but [check this course](learn-javascript.docs.this-keyword.html) for more information about this.

### Access methods
```js
const name = {
    firstName: "lucas",
    yearBirth: 1995,
    calcAge: function () {
        return 2018 - this.yearBirth;
    }
}

name.calcAge;
```
1. To call a method use the same method than properties but you may notice that methods don't need to use `()` for calling her, instead of regular function you can avoid to use `()`.

## Current errors
This is a list of the main errors that you can meet when you use Object:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.