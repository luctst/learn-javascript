---
id: executionContext
title: Execution context and execution stack
sidebar_label: Execution context and execution stack
---
> *The javascript code need to be executed in a specific environnement to work and this environnement is called execution context. An execution context in javascript is like a box, container or everything that you want which stores variables and in which a piece of our code is evaluated and executed*

## The global execution context
Okay so create a new `.js` file and added some javascript code, you opened your browser and ran your js code and you saw results so what happen ?

Well like we said javascript is executed in an environnement (execution context), by default all js code outside a function is define in the **global execution context**, we can also see execution context like an object because in javascript everything is an object in the browser the global execution context correspond to the **window object**.

## Example
```js
let a  = 'lucas';

function first() {
	let b = 'hello';
	second();
	let c = b + a;
}

function second() {
	let d = 'Hi !';
	third();
	let e = d + a;
}

function third() {
	let f = 'Hey !';
	let g = f + a;
}

first();
...
```
Let's see how this work:
1. First we create and add in the **global execution context** an `a` variable which is store into this context.
2. We create three functions `first, second, third` and we stores them in the **global execution context**.
3. Still in the **global execution context** we call the `first` function, what happen now it's we don't continue to read the code below the call of the `first` function, but we go back into this function and add on top of the execution stack (list of execution context) the **first execution context** where first is the name of function, which mean that we now execute the code inside this function.