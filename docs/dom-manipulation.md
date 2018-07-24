---
id: domManip
title: Methods to manipulate the DOM
sidebar_label: DOM manipulation
---
>*Let's now see how to manipulate the DOM with some methods*

## getElementById
This method return an object element with the element equal to the string:
```html
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
        <h1 id="mainTitle">Hello world</h1>
        <h2>Sub-title</h2>
        <h3>Third title</h3>
        <p>First p</p>
        <p>Second p</p>
        <p>Third p</p>
        <script>
            let title = document.getElementById("mainTitle");
        </script>
    </body>
</html>
```
1. We create a new variable `title`, then we use the `getElementById` method of the `document` object.
2. In `""` we use the name of the id of the element that we want access.
3. This script return an object element which contains the HTML element.
4. It's important to understand that the final result will be an object you will see later that some methods doesn't return object but htmlcollection, nodeList etc..

## getElementsByClassName
This method return an array of elements with the class selected:
```html
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
        <h1 id="mainTitle">Hello world</h1>
        <h2 class="title">Sub-title</h2>
        <h3 class="title">Third title</h3>
        <p>First p</p>
        <p>Second p</p>
        <p>Third p</p>
        <script>
            let title = document.getElementsByClassName("title");
        </script>
    </body>
</html>
```
1. Same process than above we use a variable to store our elements.
2. This time we use the class to select our elements.
3. This script will return an htmlcollection of elements.

## getElementsByTagName
This method return an htmlcollection with the tag selected:
```html
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
        <h1 id="mainTitle">Hello world</h1>
        <h2 class="title">Sub-title</h2>
        <h3 class="title">Third title</h3>
        <p>First p</p>
        <p>Second p</p>
        <p>Third p</p>
        <script>
            let text = document.getElementsByTagName("p");
        </script>
    </body>
</html>
```
1. This time we use the tag to select all our `p` tag.
2. This method return also an htmlcollection.

## querySelector
This method return an object element with the tag, class, id etc..
```html
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
        <h1 id="mainTitle">Hello world</h1>
        <h2 class="title">Sub-title</h2>
        <h3 class="title">Third title</h3>
        <p>First p</p>
        <p>Second p</p>
        <p>Third p</p>
        <script>
            let firstText = document.querySelector("h3 + p");
        </script>
    </body>
</html>
```
1. The `querySelector` method return the first element selected in `""`.
2. With this method you can target any element that you want by using your css selectors.
3. Like you can use css selectors you may know that you can target many elements but `querySelector` method only return the first element that he meet.

## querySelectorAll
This method return an object nodeList with the css selectors.
```html
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
        <h1 id="mainTitle">Hello world</h1>
        <h2 class="title">Sub-title</h2>
        <h3 class="title">Third title</h3>
        <p>First p</p>
        <p>Second p</p>
        <p>Third p</p>
        <script>
            let text = document.querySelector("p");
        </script>
    </body>
</html>
```
1. The `querySelectorAll` method works the same than `querySelector` with one differences.
2. `querySelectorAll` return all the elements that it will meet.