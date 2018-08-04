---
id: callbackHell
title: The old way, asynchronous javascript with callback functions
sidebar_label: Callback hell
---
>*In the last section we saw how asynchronous works by using callback functions which is good but there is a problem with this methods because you can cause what we called (callback hell). The cause of callback hell is when you try to write javascript in a way where execution happens from top to the bottom so when you write an ordinary javascript script.*

## Example of callback hell
```js
fs.readdir(source, function (err, files) {
  if (err) {
    console.log('Error finding files: ' + err)
  } else {
    files.forEach(function (filename, fileIndex) {
      console.log(filename)
      gm(source + filename).size(function (err, values) {
        if (err) {
          console.log('Error identifying file size: ' + err)
        } else {
          console.log(filename + ' : ' + values)
          aspect = (values.width / values.height)
          widths.forEach(function (width, widthIndex) {
            height = Math.round(width / aspect)
            console.log('resizing ' + filename + 'to ' + height + 'x' + height)
            this.resize(width, height).write(dest + 'w' + width + '_' + filename, function(err) {
              if (err) console.log('Error writing file: ' + err)
            })
          }.bind(this))
        }
      } )
    } )
  }
} );
```
1. This code is from the website [callbackhell.com](http://callbackhell.com/).
2. As you can see this kind of code is really complicated to understand because of the many callback functions.
3. There is a better way to write asynchronous javascript let's see how in the next section.

## Current errors
This is a list of the main errors that you can meet:
> **Note:** I'm not a wizard there is maybe some issue that you notice above so fell free to open an issue in the [github repo](https://github.com/luctst/learn-javascript) if you find a new error not mentioned above.