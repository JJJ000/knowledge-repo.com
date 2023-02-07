---
title: How to obtain an image data url using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The data URL of an image can be retrieved using the JavaScript FileReader API.
---

**Contents**

[TOC]

### Using the Canvas API
The Canvas API allows you to get the data URL of an image by using the `toDataURL()` method.

```javascript
var canvas = document.getElementById('myCanvas');
var ctx = canvas.getContext('2d');
var img = new Image();
img.onload = function() {
 ctx.drawImage(img, 0, 0);
 var dataURL = canvas.toDataURL();
 console.log(dataURL);
}
img.src = 'myImage.png';
```

### Using the FileReader API
The FileReader API allows you to get the data URL of an image by using the `readAsDataURL()` method.

```javascript
var reader = new FileReader();
reader.onload = function (e) {
  var dataURL = reader.result;
  console.log(dataURL);
}
reader.readAsDataURL(myImage.png);
```

### Using the XMLHttpRequest API
The XMLHttpRequest API allows you to get the data URL of an image by using the `responseType` property.

```javascript
var xhr = new XMLHttpRequest();
xhr.onload = function (e) {
  var dataURL = xhr.response;
  console.log(dataURL);
}
xhr.open('GET', 'myImage.png');
xhr.responseType = 'blob';
xhr.send();
```

### Using the Fetch API
The Fetch API allows you to get the data URL of an image by using the `blob()` method.

```javascript
fetch('myImage.png')
  .then(response => response.blob())
  .then(blob => {
    var dataURL = URL.createObjectURL(blob);
    console.log(dataURL);
  });
```
