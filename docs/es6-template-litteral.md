---
id: templateLiteral
title: Template literal string in ES6
sidebar_label: ES6 template literal
---
>*The literal template is a new way to write strings with the new ES6 syntax.*

## Template literal
```js
let name = 'lucas';
let surname = 'tostée';
const yearOfBirth = 1995;
function calculateAge(year) {
  return 2018 - year;
}

// es6 
return `${name} ${surname} a ${calculateAge(yearOfBirth)}ans.` // lucas tostée à 22ans.
```
1. To display strings with es6 you must use backtick `` and ${nameOfYourVariable} to display the content.
2. This syntax makes the content more readable.

## Current errors
This is a list of the main errors that you can meet when you use class with ES6 syntax:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.