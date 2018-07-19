---
id: startJs
title: Started with javascript
sidebar_label: Getting started with javascript
---
>*Let's write some javascript code, there are two ways of doing javascript the first one is directly in your html file and the second is by created a js file and link this file to the html file. however you'll see that the second option is the best and the most used.*

## Javascript in HTML 
The first option is directly to write Javascript in your Html file it's not the best option but it's good to test little piece of code or if you want demonstrate something. Let's see how to do that:
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8" />
    <link src=""/>
    <title>Hello world</title>
</head>
<body>
    <script>
        console.log("Hello world");
    </script>
</body>
</html>
```
1. In a html file you can write javascript code by insert the `script` tag just before the `body` closing tag.
2. After that you can write all the javascript that you want inside this tag.

## Javascript in another file
The second and the best way to do it's by creating another file with the `.js` extension and link that file in your html.
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8" />
    <link src="style.css"/>
    <title>Hello world</title>
</head>
<body>
    <h1>Hello world</h1>
    <script src="file.js"></script>
</body>
</html>
```
1. In this example we create the same Html structure than above but this time we used the `script` tag with the `src` attribute.
2. Like all `src` attribute you have to include a file with the good path to insert this file in the Html page.
3. In `script` tag the `src` attribute must contain an `.js` file.

> **Note:** - A lot of beginners do mistakes with the path of the .js file, pay attention to this.

## Current errors
This is a list of the main errors that you can meet:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.