---
id: subClass
title: Sub class with ES6
sidebar_label: ES6 subclass
---
>*ES6 introduces subclass syntax which is just an easy way to extends a class to another.*

## Subclass
When you create class you may have a class who have his own properties, methods but can also have the same than another class instead of rewrite all this methods or properties you can inherit this class with an other one.
```js
class Person = {
    constructor(name, secondName, age) {
        this.name = name;
        this.familyName = secondName;
        this.age = age;
    }

    calculateAge() {
        return  new Date().getFullYear() - this.age;
    }

    eat() {
        return `${this.name} is eating`;
    }

    static hey() {
        return `Hello world`;
    }
};

class Athlete extends Person = {
    constructor(name, secondName, age, olympicGames, medals) {
        super(name, secondName, age);
        this.olympicGame = olympicGames;
        this.medal = medals;
    }

    action() {
        return `${ super.eat() } something`;
    }

    winMedals() {
        return this.medal++;
    }
}
```
1. To inherit a class to another you have to use the `extends` keyword and the name of the parent class here `Person`.
2. Like we declare a class we use the `constructor` function in order to define properties when we will create an object based on this class, so the parameters will be our new properties.
3. Inside the `constructor` function we have a new function `super` this function is used to access and call functions on an object parent she's necessary when you use inheritance with class and must be used directly inside the `constructor` function if you want be able tu use the `this` keyword inside this class.
4. In parameters you have to call all the properties and functions of the parent class, after that you can start to use the `this` keyword to define your own new properties.
5. As you may seen we created a new function inside the `Athlete` class and we use the `super` keyword to call the `eat` function of the `Person` class, you can also access to the functions parent with the `super` keywords which is this time not a function but an object.