---
title: Using jquery to set the background image with css
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: jQuery can set a background-image using the css() method.
---

**Contents**

[TOC]

## Section 1: Setting background-image

Using jQuery, you can set the background-image of an element using the `css()` method. This method accepts two parameters: the property name and the value to set. To set the background-image, the property name should be `background-image` and the value should be a valid URL or data URI.

## Section 2: Example

The following example shows how to set the background-image of an element with an ID of `myElement` to a URL:

```javascript
$('#myElement').css('background-image', 'url(http://example.com/myImage.jpg)');
```

## Section 3: Multiple Background Images

In some cases, you may want to set multiple background images for an element. To do this, you can use the `background` property instead of `background-image`. The value of this property should be a comma-separated list of valid URLs or data URIs.

## Section 4: Example

The following example shows how to set two background images for an element with an ID of `myElement`:

```javascript
$('#myElement').css('background', 'url(http://example.com/myImage1.jpg), url(http://example.com/myImage2.jpg)');
```
