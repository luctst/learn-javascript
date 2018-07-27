---
id: spread
title: ES6 spread operator
sidebar_label: ES6 spread operator
---
>*The spread operator is a new syntax sugar who allow the elements to expand let's see some examples.*

## Spread operator
```js
// Insert array
var arr = [3,4];
var mid = [1,2,...arr];
return mid; // [1,2,3,4]

// Copy array
var tab = [1,2];
var tab2 = [...tab];

return tab2; // [1,2]

tab2.push('d'); // tab2 = [1,2,d]
return tab; // [1,2]

// Insert string
var char = 'hello';
var arr = [...char];
return arr; // ['h','e','l','l','o'];
```
1. In the first example you can include array in an other array by using the spread operator who will include the elements in array instead of nested as you can see.
2. The spread operator allow us to copy array as you may know when you're using `=` to copy an object to an other object you don't create a copy but a reference which means that each operation you made on this reference will be also on the initial object, the spread operator can inverse this.
3. The spread operator also allow us to insert string in array like in our third example.

## Current errors
This is a list of the main errors that you can meet with the spread operator syntax:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.
