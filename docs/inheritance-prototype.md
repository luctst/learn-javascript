---
id: prototypeChain
title: Inheritance and prototype chain
sidebar_label: Prototype chain
---
>*In javascript everything is an object, well almost everything like we saw at the beginning of this courses there is also primitives where you can check by [clicking here](learn-javascript/docs/dataType.html), everything else is an object (array, function, object, date, ..)*

## Class
Object can interact each other via inheritance, you can if you want create a `class` which is like a model where each instance of this class will inherit of his properties and methods.
> **Note** - [Check this curses to learn how to create class](learn-javascript/docs/class.html).

## Prototype chain
Each object in javascript has a property which is called `prototype`, inheritance is possible because of that properties.

Like all object have this `prototype` properties add all your methods and properties in this `prototype` property to inherit from all the other objects.

This is how inheritance works in javascript at the root of this chain there the Object `object` which group of the properties and methods that object have access. This is why it's possible for an array to access methods like (length,push,pull etc..).

## Summary
Every javascript object has a prototype property, which makes inheritance possible in javascript.

The prototype property of an object is where we put methods and properties that we want other objects to inherit.

The constructor prototype property is not the the prototype of the constructor itself, it's the prototype of all instances that are created through it.

When a certain method ( or property ) is called, the search starts in the object itself, and if it cannot be found, the search moves on to the object's prototype. This continues until the method is found: prototype chain.

## Current errors
This is a list of the main errors that you can meet:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.