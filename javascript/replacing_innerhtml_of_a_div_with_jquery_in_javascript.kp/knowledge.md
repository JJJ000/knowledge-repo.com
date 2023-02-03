---
title: What is the syntax for changing the content of a div using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the jQuery .html() method to replace the innerHTML of a div.
---

**Contents**

[TOC]

**Section 1: Prepare the HTML**

To replace the innerHTML of a div using jQuery, you need to have an HTML element with the `div` tag.

```html
<div id="example">
  <p>This is the original content</p>
</div>
```

**Section 2: Include jQuery**

Next, you need to include jQuery in your HTML document. This can be done by adding the following script tag to the `<head>` element:

```html
<script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
```

**Section 3: Select the Element**

Now that you have the HTML and jQuery included, you can select the element you want to replace the innerHTML of. This can be done using the jQuery `$()` function and passing in the `id` of the element you want to select.

```javascript
const element = $('#example');
```

**Section 4: Replace the InnerHTML**

Finally, you can use the jQuery `.html()` function to replace the innerHTML of the element. This can be done by passing in the new HTML as a string to the `.html()` function.

```javascript
element.html('<p>This is the new content</p>');
```
