---
id: class
title: Class in ES6
sidebar_label: ES6 class 
---
>*ES6 class is a new powerful way to create class.*

## Class
```js
class Person {
  constructor(name,lastName,job,year) {
    this.name = name;
    this.lastName = lastName;
    this.job = job;
    this.year = year;
  }
  
  calculateAge() {
    2018 - this.year;
  }
  
  static hey() {
    return 'Hello world !!';
  }
}

let Lucas = new Person('lucas','Tostée','Developer',1995);
Lucas.calculateAge(); // 22
Lucas.hey(); // Error !!!!
```
1. to declare classes you can use the keyword `class`, in this one you can also use the `constructor` function who works like the constructor function es5 but directly inside your class.
2. With es6 you can directly declare your method in your class, and use keyword like `static `who block the inheritance.


## Current errors
This is a list of the main errors that you can meet when you use class with ES6 syntax:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.