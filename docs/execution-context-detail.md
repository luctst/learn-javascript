---
id: executionContextDetail
title: Execution context in detail.
sidebar_label: Execution context in detail
---
> *We saw in the last chapter when a new execution context is created, let's see now what happen in this execution context.*
 *An execution context contains three properties:*
 >- The variable object who store `functions`.
 >- The scope chain who store `variables` and `parents variables`.
 >- And the this variable.
> *When a function is called a new execution context is put on top of the execution stack, inside this one there are two phases.*

## Creation phase
During this phase we define the properties of the execution context which we already defined above, the first one is

### Variable object
- First, the argument object is created containing all the arguments that were passed into the function.
- Second, the code is scanned for functions declarations and for each function a property is created in the variable object, pointing to the function.
- Third, the code is scanned for variable declarations and for each variable a property is created in the variable object and set to undefined.

### Scope chain
This section deserve an entire lesson so [check this links](learn-javascript/docs/scope-chain.html) to understand how scope chain works.

### This variable
You can find more details to this section by checking this file [this keyword](learn-javascript/docs/this-keyword.html)

## Execution phase
During this phase the code is executed line by line.

## Current errors
This is a list of the main errors that you can meet when you use data types:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.