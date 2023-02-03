---
title: Altering the image source using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the jQuery .attr() method to set the `src` attribute of the image element to the desired image source.
---

**Contents**

[TOC]

##Section 1: Selecting the Image

Using jQuery, you can select the image you want to change the source of using the `$()` function. For example, if you want to select an image with the ID `myImage`, you could use the following code:

```
$('#myImage')
```

##Section 2: Changing the Source

Once you have selected the image, you can use the `attr()` function to change the source. For example, if you want to change the source to `example.jpg`, you could use the following code:

```
$('#myImage').attr('src', 'example.jpg');
```

##Section 3: Adding an Event Handler

If you want to change the source of the image when a certain event occurs, you can add an event handler to the image. For example, if you want to change the source when the user clicks on the image, you could use the following code:

```
$('#myImage').click(function() {
    $(this).attr('src', 'example.jpg');
});
```

##Section 4: Adding a Fade Effect

If you want to add a fade effect when changing the source of the image, you can use the `fadeOut()` and `fadeIn()` functions. For example, if you want to fade out the old image and fade in the new image when the user clicks on the image, you could use the following code:

```
$('#myImage').click(function() {
    $(this).fadeOut(500, function() {
        $(this).attr('src', 'example.jpg').fadeIn(500);
    });
});
```
