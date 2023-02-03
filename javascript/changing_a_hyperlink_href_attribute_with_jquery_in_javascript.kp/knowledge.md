---
title: What is the syntax for altering the href of a hyperlink using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the jQuery attr() method to change the href attribute for a hyperlink.
---

**Contents**

[TOC]

**Section 1: Include the jQuery Library**

In order to use jQuery in your Javascript code, you must first include the jQuery library. This can be done by adding a script tag to the HTML page that references the jQuery library.

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
```

**Section 2: Select the Hyperlink Element**

In order to change the href attribute of the hyperlink, you must first select the element using jQuery. This can be done using the jQuery `$()` selector.

```js
var link = $('a');
```

**Section 3: Change the href Attribute**

Once the element is selected, you can use the `attr()` method to change the href attribute.

```js
link.attr('href', 'http://example.com');
```

**Section 4: Test the Change**

Finally, you can test the change by clicking on the link and verifying that the URL has been updated.
