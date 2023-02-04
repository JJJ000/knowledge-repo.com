---
title: Replacing broken images using jquery/javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: jQuery can be used to replace broken images by using the .attr() method to update the `src` attribute of the image element.
---

**Contents**

[TOC]

# Section 1: jQuery Solution

To replace broken images using jQuery, you can use the `.error()` method. This method is triggered when an image fails to load. The code below will replace broken images with a placeholder image:

```js
$('img').error(function(){
    $(this).attr('src', 'placeholder.jpg');
});
```

# Section 2: JavaScript Solution

To replace broken images using JavaScript, you can use the `onerror` event handler. This event handler is triggered when an image fails to load. The code below will replace broken images with a placeholder image:

```js
var imgs = document.getElementsByTagName('img');
for (var i = 0; i < imgs.length; i++) {
    imgs[i].onerror = function() {
        this.src = 'placeholder.jpg';
    }
}
```

# Section 3: Benefits of jQuery

Using jQuery to replace broken images has the advantage of being more concise and easier to read. It also allows you to use the same code to replace multiple images at once.

# Section 4: Benefits of JavaScript

Using JavaScript to replace broken images has the advantage of being more flexible. It allows you to customize the code to replace a specific image, or to take a different action when an image fails to load.
