---
title: Using jquery to load images in advance
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: jQuery can preload images by creating a new Image object and setting its source to the image`s URL.
---

**Contents**

[TOC]

# Section 1: Preloading Basics
Preloading images with jQuery is a simple process. The basic idea is to create a new Image object, set the source of the image to the URL of the image you want to preload, and then add the image to the DOM. This will cause the browser to start loading the image in the background.

# Section 2: jQuery Preload Function
The jQuery library provides a helpful function for preloading images. The function is called $.preloadImages(). It takes an array of image URLs as an argument and preloads each image.

# Section 3: Preloading Example
Here is an example of how to use the $.preloadImages() function to preload a single image:

```javascript
var imageURL = "https://example.com/image.jpg";

$.preloadImages(imageURL, function(){
    // Image is now preloaded
});
```

# Section 4: Preloading Multiple Images
You can also use the $.preloadImages() function to preload multiple images at once. Here is an example of how to preload multiple images:

```javascript
var imageURLs = [
    "https://example.com/image1.jpg",
    "https://example.com/image2.jpg",
    "https://example.com/image3.jpg"
];

$.preloadImages(imageURLs, function(){
    // Images are now preloaded
});
```
