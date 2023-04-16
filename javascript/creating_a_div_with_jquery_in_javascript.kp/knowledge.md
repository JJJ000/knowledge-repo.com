---
title: Constructing a div element using jquery
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In jQuery, a div element can be created using the $(`<div>`) syntax.
---

**Contents**

[TOC]

1. Syntax:
```javascript
$('<div/>');
```

2. Example:
```javascript
$('<div/>', {
    id: 'example-div',
    class: 'example-class',
    text: 'Example text'
});
```

3. Result:
```html
<div id="example-div" class="example-class">Example text</div>
```

4. Usage:
```javascript
$('body').append($('<div/>', {
    id: 'example-div',
    class: 'example-class',
    text: 'Example text'
}));
```
