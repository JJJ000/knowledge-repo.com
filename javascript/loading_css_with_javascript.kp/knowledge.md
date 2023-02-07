---
title: What is the process for incorporating css files into a JavaScript program?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the HTML <link> tag in a <script> tag to load CSS files using Javascript.
---

**Contents**

[TOC]

1. **Create a <link> Element:**

Create a <link> element and set its attributes to point to the CSS file you wish to load. The <link> element should be placed in the <head> of the HTML document.

```html
<link rel="stylesheet" type="text/css" href="style.css">
```

2. **Create a <script> Element:**

Create a <script> element and set its attributes to point to the Javascript file containing the code to load the CSS file.

```html
<script type="text/javascript" src="script.js"></script>
```

3. **Write the Javascript Code:**

Write the Javascript code to dynamically create the <link> element and append it to the <head> of the HTML document.

```javascript
var linkElement = document.createElement("link");
linkElement.rel = "stylesheet";
linkElement.type = "text/css";
linkElement.href = "style.css";
document.head.appendChild(linkElement);
```

4. **Include the <script> Element:**

Finally, include the <script> element in the HTML document so that the code to load the CSS file will run.

```html
<html>
  <head>
    <script type="text/javascript" src="script.js"></script>
  </head>
  <body>
  </body>
</html>
```
