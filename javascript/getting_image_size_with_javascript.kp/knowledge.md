---
title: What is the syntax for finding the height and width of an image using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can get the image size (height & width) using the JavaScript method `.naturalWidth` and `.naturalHeight` on an image object.
---

**Contents**

[TOC]

# Section 1: Using the Image Object

The simplest way to get the image size (height & width) using JavaScript is to use the `Image` object. The `Image` object is a built-in JavaScript object that can be used to represent an image file. 

# Section 2: Creating the Image Object

To create an `Image` object, you can use the `new` keyword and pass in the URL of the image as an argument. For example: 

```javascript
let img = new Image();
img.src = 'https://example.com/image.jpg';
```

# Section 3: Accessing the Image Size

Once the `Image` object has been created, you can access the image size (height & width) using the `naturalWidth` and `naturalHeight` properties. For example: 

```javascript
let width = img.naturalWidth;
let height = img.naturalHeight;
```

# Section 4: Using the onload Event

It is important to note that the `naturalWidth` and `naturalHeight` properties will not be set until the image has finished loading. To ensure that the image has finished loading, you can use the `onload` event. For example: 

```javascript
img.onload = function() {
  let width = img.naturalWidth;
  let height = img.naturalHeight;
  // Do something with the image size
};
```
