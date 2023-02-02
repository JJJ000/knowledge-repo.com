---
title: View an image prior to submitting it
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: It is possible to display a preview of an image before it is uploaded by using the FileReader API in Javascript.
---

**Contents**

[TOC]

# Solution 1:
## Using FileReader
The FileReader API can be used to preview an image before it is uploaded. This is done by creating a FileReader object and setting the `onload` event to a function that will render the image.

```javascript
var reader = new FileReader();
reader.onload = function (e) {
    document.getElementById("preview").src = e.target.result;
};
```

# Solution 2:
## Using URL.createObjectURL
The URL.createObjectURL API can also be used to preview an image before it is uploaded. This is done by creating a URL object and setting the `src` attribute of an image element to the URL.

```javascript
var url = URL.createObjectURL(file);
document.getElementById("preview").src = url;
```
