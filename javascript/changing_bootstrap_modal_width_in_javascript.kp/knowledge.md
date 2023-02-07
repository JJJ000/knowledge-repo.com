---
title: What is the procedure for altering the default width of a twitter bootstrap modal box?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can set the width of the modal box by using the jQuery `.modal(`option`, `width`, <value>)` function.
---

**Contents**

[TOC]

#1. Change Bootstrap CSS

The default width of a Bootstrap modal box can be changed by editing the Bootstrap CSS file. In the Bootstrap CSS, look for the `.modal-dialog` class and change the `width` property as desired.

#2. Use Custom CSS

Alternatively, you can use custom CSS to override the Bootstrap CSS. Create a custom CSS file and add the following code to it:

```css
.modal-dialog {
    width: [desired width];
}
```

#3. Include Custom CSS File

Include the custom CSS file in your HTML document by adding the following line of code in the `<head>` section:

```html
<link rel="stylesheet" href="[path to custom CSS file]">
```

#4. Refresh Page

Finally, refresh the page to apply the changes. The modal box should now have the desired width.
