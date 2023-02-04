---
title: Find the tag name of the selected element using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The selected element`s tag name can be retrieved using the jQuery function `$(selector).prop(`tagName`)`.
---

**Contents**

[TOC]

1. Selecting an Element

To select an element in jQuery, you can use the jQuery selector function. The syntax for this is `$(selector).` This can be used to select an element by its id, class, tag name, or other attributes.

2. Get Tag Name

Once you have selected an element, you can use the jQuery `.prop()` method to get the tag name of the element. The syntax for this is `$(selector).prop('tagName')`. This will return the tag name of the element as a string.

3. Example

For example, if you wanted to get the tag name of an element with the id "myElement", you could use the following code: 

```js
var tagName = $('#myElement').prop('tagName');
```

4. Output 

This will return the tag name of the element as a string, e.g. `"DIV"` or `"SPAN"`.
