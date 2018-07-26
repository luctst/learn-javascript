---
id: booleanLogic
title: Boolean logic
sidebar_label: Boolean logic
---
>*The boolean logic is simply operators who returns an boolean `true` or `false`, we use this syntax most of the time for conditional.*

## The AND operator
The and operator is represent with this syntax `&&` for this return `true` the all the conditions that you create must be `true` otherwise the AND operator will return false:
```js
let age = 23;

if ( age >= 20 && age < 30 ) {
    return `You're a man now !!`;
} else {
    return "You're still a child";
}
```
1. In this example we create a variable to test our AND operator, we give to this variable the value `23`.
2. We now use an if / else statement to check something, with the AND operator we need to have the conditions true and in this example it's okay because `age` is greater than 20 and also inferior at 30 so our both conditions our true the result will be `You're a man now !!`.
3. If one of our conditions will be not true the result will be `You're still a child`.

## The OR operator
We saw above the AND operator who check if all the conditions are true, well with the OR operator is a little bit different you can have only one conditions true for this return `true`.
```js
let age = 23;

if ( age >= 20 || age <= 15 ) {
    return `You're a man now !!`;
} else {
    return "You're still a child";
}
```
1. We will use the same code than above for our demo, to use the OR operator you have to use this `||` syntax which is not the `l` letter in lowercase.
2. In this condition we ask if `age` is greater than 20 and the answer is yes OR if age is inferior than 15 which is false so we can see our if like this `(true || false)`. The result of this condition will be `You're a man now`.
3. Like we said earlier with the OR operator as long as one condition is true the result will always be true.

## The NOT operator
The NOT operator is different from the two above because this one will not check if this condition is true or false or everything else this operator will simply inverse the actual value:
```js
let isAdult = true;

if ( !isAdult ) {
    return "You're still a child";
} else {
    return `You're a man now !!`;
}
```
1. We create a new variable `isAdult` and we give this variable a boolean `true`.
2. In the if / else statement we ask if  `isAdult` is equal to true which is in this case yes, but you may notice that we also use this `!` syntax who is equal to the NOT operator and inverse the value, so in this case the `isAdult` variable is now equal to `false` so the result will be `You're still a child`.