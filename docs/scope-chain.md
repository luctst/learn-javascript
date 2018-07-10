---
id: scopeChain
title: Scope chain
sidebar_label: The scope chain phase
---
>*What is scope chain ? Scoping answer the question "Where you can access a certain variable ?"*
>*In javascript each new function create a new scope instead of some others programming languages like PHP,* >*JAVA etc.. where even an `if`, `for` elements create a new scope.*
>*A scope is determined where the function is written.*
>*Let's see some examples to really understand how scope works.*

## First example
```js
let a = "hello";
first();

function first() {
    let b = "hi !";
    second();

    function second() {
        let c = "hey !";
        console.log( a + b + c);
    }
}
```
1. Like the global execution context there is a global scope which is the scope by default in our example the global scope has access to the `a` variable and also to the `first` function.
2. We got the first local scope which is the code inside the `first` function, it means that we can access to the code inside the `first` function and to his parent scope which is the global scope.
3. Inside the `first scope` we call an other function `second` which is defined in the scope of the `first` function. We now execute the code inside the `second` function.
4. We execute the `console.log` function who returns the `a`, `b` and `c` variable, but we don't have access to the `a` and `b` variable so the computer will find in the parent scope if it can find the two variables.
5. The scope chain works in descending order, you can access variable of a parent scope and not the opposite.

## Current errors
This is a list of the main errors that you can meet when you use scope chain:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.