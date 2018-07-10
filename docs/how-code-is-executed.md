---
id: codeExecuted
title: How the javascript code is executed
sidebar_label: How code is executed
---
> *Like we know javascript is a client-side language which mean that we don't have to interact with a server to play with js instead of that every browser has an engine who stores the javascript and executed it. In this lesson we will not cover how the javascript browser engine work but what happen in this engine.*

## Parse the code
The first thing that the engine will do is parse your javascript code, which means that it will check if your js code is valid no errors, good structure etc.. So the parser know the javascript rules, if everything is correct it will produces a data structure known as the abstract syntax three.

## The machine code
You may know that computer only understand the machine code (binary) but from now we don't write this binary code so how is it possible that the browser understand our javascript code ? Well when the parser produces the abstract syntax three it will then translated this structure in machine code.

## Code runs
To this point we now have a code that our computer can understand so here we go our code is executed by the computer, perfect :)

## Javascript engine
Like i said above all the browser don't use the same engine to make javascript work, we will not cover how this engine work it's too long and more difficult but i'm gonna list all the main engine use in the main browser, if you want know more about them check on the web:
- **Google:** V8 engine.
- **Safari:** JavascriptCore engine.
- **Ie:** Chakra engine.
- **Mozilla:** SpiderMonkey engine.
- **Opera:** Cakaran engine.

## Current errors
This is a list of the main errors:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.

## Current errors
This is a list of the main errors that you can meet when you javascript engine:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.