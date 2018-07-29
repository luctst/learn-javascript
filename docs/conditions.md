---
id: statement
title: If / else statements
sidebar_label: If / else conditions
---
>*Conditional statements allow us to perform different actions based on different condition.*

## If / else statements
```js
let name = "Lucas";
let status = "single";

if (status === "single") {
    console.log(`${name} is single `);
}
```
1. The conditions in javascript works in two steps, the first one is to check if the condition that you write is true or false and the second to execute the code.
2. To write your condition after the `if` keyword open `()` and write your code, the javascript engine will now check if your condition is true if it does then we can go to the second step.
3. So your condition is true so now we can execute the located inside the `{}`.

```js
let name = "Lucas";
let status = "married";

if (status === "single") {
    console.log(`${name} is single `);
} else {
    console.log(`${name} is married`);
}
```
1. For this example we change the value of our `status` variable and add a else condition.
2. So now our condition is now equal to false it means that we can't execute the code inside the first `{}` so the javascript engine will execute the second line which is `else`.
3. With else you can't add condition it means that if the if condition is false the code will always execute the else condition. we'll see now how to check many conditions.

## If / else if / else statement
```js
let name = "Lucas";
let status = "married";

if (status === "single") {
    console.log(`${name} is single `);
} else if (name === "Lucas") {
    console.log(`Your name is ${name}`);
} else {
    console.log(`${name} is married`);
}
```
1. We saw above how to check one condition but let's see now how to check many conditions.
2. We use a new keywords here `else if` who allow us to check another condition so right here if the first `if` condition is false the js engine will check if the `else if` condition is true if it does then it will execute the code, if the condition is false it will execute the `else` condition.
3. In this example we used only one `else if ` condition but you can add as much as you want `else if ` condition.

## Current errors
This is a list of the main errors that you can meet:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.