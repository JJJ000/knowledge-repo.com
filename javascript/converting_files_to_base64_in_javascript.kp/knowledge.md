---
title: What is the process for encoding a file to base64 in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the FileReader API to read the file as a base64-encoded string.
---

**Contents**

[TOC]

# Section 1: Using FileReader

The FileReader object lets web applications asynchronously read the contents of files stored on the user's computer, using File or Blob objects to specify the file or data to read.

To convert a file to base64 (that is, to read the contents of the file and convert them to base64), we can use the FileReader object.

# Section 2: Example

The following example shows how to convert a file to base64 by using the FileReader object.

```javascript
// Create a FileReader object
var reader = new FileReader();

// Read the file as a data URL
reader.readAsDataURL(file);

// When the file is read it triggers the onload event
reader.onload = function () {
   // The file data is contained in this.result
   var base64 = this.result;
};
```

# Section 3: Using toDataURL

The canvas element also has a toDataURL() method that can be used to convert an image file to base64.

# Section 4: Example

The following example shows how to convert an image file to base64 by using the toDataURL() method.

```javascript
// Create a new image
var image = new Image();

// Set the source of the image to the file that you wish to convert
image.src = file;

// When the image has loaded, trigger the onload event
image.onload = function () {
   // Get a canvas object
   var canvas = document.createElement('canvas');

   // Set the canvas to the same dimensions as the image
   canvas.width = image.width;
   canvas.height = image.height;

   // Draw the image onto the canvas
   canvas.getContext('2d').drawImage(image, 0, 0);

   // Get the base64 data from the canvas
   var base64 = canvas.toDataURL();
};
```
