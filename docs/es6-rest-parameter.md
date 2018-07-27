---
id: rest
title: ES6 rest parameter
sidebar_label: ES6 rest parameter
---
>*The spread operator is used in a function as an arguments, this syntax allow us to represent an undefined numbers of arguments who will be add in an array.*

## Rest parameter
```js
function isFullAge(...years) {
  for(let i of years) {
    return (2018 - i) >= 18;
  }
}
isFullAge(1998,1997,1996,1995); // return True,true,true,true
```

## Current errors
This is a list of the main errors that you can meet with the rest parameter syntax:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.
