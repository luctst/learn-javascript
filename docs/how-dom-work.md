---
id: domWork
title: What is DOM events
sidebar_label: DOM events
---
>*An event is a kind of notification that are sent to notify the code that something happened on the webpage, for example when you click on a button, resizing a window, scroll etc.. In javascript we use event listener to do event, it's a function that performs an action based on a certain event, it waits for a specific event to happen.*

## Message queue
The message queue environment is like a box where all the event that happen in the browser are put.

## Event listener
We saw earlier how the execution stack works well here it's the same once that the execution stack is **empty** the message queue put on top of the execution stack the first event that he meet. But when an event listener comes in a message queue ? Well each time that this function is called, she's put on top of the message queue environment and go in the execution stack once this one is empty.

## Current errors
This is a list of the main errors that you can meet:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.