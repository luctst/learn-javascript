---
id: constructor
title: Creating objects, function constructors
sidebar_label: What is a constructor in object
---
>*You will probably create a lot of objects, and sometimes you may have some properties or methods that you will use in other objects, it will be really cool if you wan simply give methods, properties to different objects without rewrite them. Well you can do that with the constructor function.*

## Function constructor
```js
const Person = function (name, yearOfBirth, job) {
    this.name = name;
    this.yearOfBirth = yearOfBirth;
    this.job = job;
};
```
1. Until now for create objects we always used the object literal way and it's good but you can't do inheritance with this methods so one solution is to use the `constructor` function to allow inheritance between objects.
2. The `constructor` function is simply a function as you can see above with parameters who will be the properties of our object that we will create later, so you have to use `this` in order to create this properties. But if you remember we saw in our previous section on the this keyword that when use in a regular function this return the `window` object so how is it possible this properties point to our new object ? We'll see that in the next section.

## The new keyword
```js
const Lucas = new Person("Lucas",1995,"web-developer");
```
1. We saw above that the `this` keyword will point to the `window` object and that's a problem we want that when we call the `Person` function the parameter's become properties and create a new object, fortunately we have the `new` keyword who do everything for us.
2. When you use `new`, a new empty object will be created which will be called in our example `Lucas`, after that the `new` keyword will called the function written after him so in our case the `Person` function. We now have a new object `Lucas`, and properties because the function now point to the new object that we have just created.
3. So now we can quickly create new object with properties by using this method and it's really simple and better because you can keep your code clear and organize.

## Inherit methods
Until now we only use properties but how we can do to inherit methods for all our objects ?
```js
const Person = function (name, yearOfBirth, job) {
    this.name = name;
    this.yearOfBirth = yearOfBirth;
    this.job = job;
};

Person.prototype.calculateAge = () => {
    return new Date().getFullYear() - this.yearOfBirth;
}

const Lucas = new Person("Lucas",1995,"web-developer");
const Jane = new Person("Jane",1994,"secretary");
const Mark = new Person("Mark",1993,"designer");

Lucas.calculateAge(); // 23
Jane.calculateAge(); // 24 
Mark.calculateAge(); // 25
```
1. One way to do that is to add our function in our function constructor `Person` but it's not the best way because if we have a lot of functions it will be really hard to maintain, so the solution is to use the `prototype` property like we saw in the previous section.
2. We know that all objects have the `prototype` property so we gonna use this one for inherit our methods, because our `Person` function constructor is an object.
3. By creating our method `calculateAge` in the `prototype` property of our `Person` function constructor all our objects that we created with this function inherit this method.

## Current errors
This is a list of the main errors that you can meet:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.