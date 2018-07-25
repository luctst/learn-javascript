---
id: module
title: Modules in ES6
sidebar_label: ES6 modules
---
>*ES6 introduces a new kind of syntax which is `export` and `import` a lot of programming languages can export data from another files with functions but javascript couldn't before ES6 it's now possible to add data like object, functions, variables etc.. from another file, let's see how to use this new stuff.*

In javascript there are many ways of import and export we can use the:
* Default export.
* Names export.

We will use this simple structure to illustrate our examples:
```bash
└── model/
    ├── file.js 
├── index.js
```

## Default export
This kind of export is really helpful when you want export only one thing (string, object, functions etc..).
```js
// file.js
export default const string = "Hi, I'm lucas";
```
```js
// index.js
import string from "./model/file";
return string; // Hi, I'm lucas
```
1. In our `file.js` we use the `export default` syntax before the element that we want export.
2. In our `index.js` file we use the `import` syntax and the name of our value plus the file where the export is located.
3. After that you can use this value as you want in the `index.js` file.
4. You may notice that we do not give an `.js` extension when we import our data it's because javascript understand that we talk about js so you can avoid the extension name.
5. As you can see when you import data from an export default you can change the name of the value that you import, in this example we use the same name `string` but you can if you want in the import line use `str` or everything else it will also work.
6. Finally we use a string as example here but you can export all types of data like objects, functions, number etc..

## Export with name
This export way is really helpful when you want export many data:
```js
// file.js
export const sum = (a, b) => {
    return a + b;
}
export const mutliply = (c, d) => {
    return c * d;
}
```
```js
// index.js
import { sum, multiply } from "./model/file";
return `Calculate the sum ${ sum(2, 2) }, and multiply by ${ multiply(3, 3) }`;
```
1. For this export we simply use the `export` keyword before our element.
2. To import this data you have to use `{}` and enter the exact same name, it's important because with export default you can rename your data but with this method you can't you have to give the exact same name.
3. After that you can use your new import data as you want.

## Rename your export name individually
We saw in the last section that you have to give the exact same name for this to work, but there is one way to change the name of your import and let's see how:
```js
// file.js
export const sum = (a, b) => {
    return a + b;
}
export const mutliply = (c, d) => {
    return c * d;
}
```
```js
// index.js
import { sum as s, multiply as m } from "./model/file";
return `Calculate the sum ${ s(2, 2) }, and multiply by ${ m(3, 3) }`;
```
1. We will use the same example than above for this demo.
2. To rename your import simply use the `as` keyword following by the new name here `s` and `m` and use this new name to call your data.

## Import all our export names
Imagine that you have a lot of export name it will be really complicated and long to write all this export, so there is a better way for import everything just once.
```js
// file.js
export const sum = (a, b) => {
    return a + b;
}
export const mutliply = (c, d) => {
    return c * d;
}
```
```js
// index.js
import * as importAll from "./model/file";
return `Calculate the sum ${ importAll.sum(2, 2) }, and multiply by ${ importAll.multiply(3, 3) }`;
```
1. For import everything just once you have to use `*` syntax following by his name, this will create an object where all your export name will be methods and properties.
2. From now to call our methods or properties use the `.` notation like you always did.