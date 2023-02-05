---
title: Replace the current image at the same url with a new one
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Reload the page or use the JavaScript function `location.reload()` to refresh the image.
---

**Contents**

[TOC]

# Section 1: Reloading the Image

The simplest way to refresh an image in Javascript is to reload the image with a new one at the same URL. This can be done by setting the `src` attribute of the `<img>` element to the same URL as before. This will cause the browser to make a new request to the server for the image, which will be returned with the new version.

```javascript
var imgElement = document.getElementById('myImage');
imgElement.src = imgElement.src;
```

# Section 2: Caching Issues

One issue with this approach is that the browser may cache the image, so the new version might not be loaded. To prevent this, you can add a unique query string to the end of the URL. This will cause the browser to make a new request to the server and not use the cached version.

```javascript
var imgElement = document.getElementById('myImage');
imgElement.src = imgElement.src + '?v=' + Date.now();
```

# Section 3: Preloading Images

Another approach is to preload the new image and then set the `src` of the `<img>` element to the new image’s URL. This will ensure that the new image is loaded and displayed immediately.

```javascript
var imgElement = document.getElementById('myImage');

var newImage = new Image();
newImage.src = 'https://example.com/image.jpg';

imgElement.src = newImage.src;
```

# Section 4: Using Promises

Finally, you can use the `fetch()` API to make a request for the new image, and then set the `src` of the `<img>` element to the new image’s URL. This approach allows you to use Promises to handle the asynchronous loading of the image.

```javascript
var imgElement = document.getElementById('myImage');

fetch('https://example.com/image.jpg')
  .then(function(response) {
    return response.blob();
  })
  .then(function(imageBlob) {
    imgElement.src = URL.createObjectURL(imageBlob);
  });
```
