---
id: loop
title: Loop and iteration
sidebar_label: Loop and iteration
---
>*Loop offer a quick and easy way to do something repeatedly, you can think of a loop as a computerized version of the game where you tell someone to take X steps in one direction then Y steps in another. There are many ways to do loop in js let's see all this methods.*

You will see that we have many ways to declare loops in javascript but all works exactly the same in the background:

1. The first step in a loop is the initialization we declare or we use a variable generally `i` it's a kind of convention, and we give her a value.
2. The second is the condition, this will return a boolean if the result is true we can continue through the loop steps if it's false then we stop the process.
3. The last step is the final expression this will be evaluated at the end of each loop iteration.

## for loop
The syntax for loop is really useful when you want to cross an element whose size you know.
```js
for (let i = 0; i < 10; i++) {
    console.log(i);
}
```
1. Let's see this basic for loop in details.
2. We initialize our variable with a value of `0`.
3. We now check if the condition is true and it is because `i ` = `0` and `0` is inferior to `10`.
4. The condition is true we can execute the code inside our loop.
5. The final step is the last statement we can now increment our variable `i++` so from now `i` is equal to `1`.
6. The process is done we can repeat all this steps until the condition is false.

## While loop
The while loop syntax is useful when you have an element with a size that you ignore.
```js
let i = 0;
while( i < 10) {
    console.log(i);
    i++;
}
```
1. The while loop works the same than for loop but with a different syntax.
2. You have to initialize your variable outside the while condition.
3. Use the `while` keyword and write your condition.
4. Write your code inside the while `{}`.
5. Don't forget to add at the end of the while statement the last step `i++` or you will have an infinite loop and it will block your web browser.

## ForEach loop
The forEach loop is a little bit different because she is available only when it's an collection of a DOM element.
```js
DomElement.forEach( el => {
    console.log(el);
} );
```
1. Once you've got a collection of a DOM element you have access to the `forEach` method who works like a loop.
2. You have to declare one parameter who can be equal to the `i` variable seen above.

## Continue statement
The continue instruction allow us to skip the execution of the loop at a certain moment.
```js
let noms = ["lulu","bubu","tutu",23,"riri"];
for (let i = 0; i < noms.length; i++) {
    if ( typeof noms[i] !== String) {
        continue;
    } else {
        console.log(noms[i]);
    }
};
```
1. The javascript loop add a couple of instructions like the `continue` keywords.
2. In our example we use the `continue` keywords to skip the element which is different from a `String` data type.
3. The result in the console will be `lulu bubu tutu riri`.

## Break statement
The continue instruction allow us to stop the execution of the loop at a certain moment.
```js
let noms = ["lulu","bubu","tutu",23,"riri"];
for ( let i = noms.length -1; i >= 0; i-- ) {
    if ( typeof noms[i] !== String ) {
        break;
    } else {
        console.log(noms[i]);
    }
}
```
1. The `break` keyword is the opposite of the `continue` keyword.
2. The `break` keyword will stop the execution of the loop when an element of the `noms` array will be different from a `String` data type.

## Current errors
This is a list of the main errors that you can meet when you use loop:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.