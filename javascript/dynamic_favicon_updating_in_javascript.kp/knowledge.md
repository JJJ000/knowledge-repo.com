---
title: Altering the website favicon in real-time
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The favicon of a website can be dynamically changed using JavaScript by manipulating the document.head.querySelector(`link[rel=`shortcut icon`]`).href property.
---

**Contents**

[TOC]

#### Solution

1. **Create a new favicon**

Create a new favicon using an online favicon generator or any other design tool. Save the favicon as a .ico file.

2. **Upload the favicon**

Upload the favicon to a web server and make sure it is publicly accessible.

3. **Add the favicon to the HTML**

Add the following code to the `<head>` section of the HTML document:

```html
<link rel="shortcut icon" href="path/to/favicon.ico" type="image/x-icon" />
```

Where `path/to/favicon.ico` is the URL of the uploaded favicon.

4. **Change the favicon dynamically**

To change the favicon dynamically, use JavaScript to change the `href` attribute of the `<link>` element in the `<head>` section of the HTML document. For example:

```javascript
document.querySelector('link[rel="shortcut icon"]').href = 'path/to/new/favicon.ico';
```
