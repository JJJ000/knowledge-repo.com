---
title: When a textbox is focused on, highlight all of its contents (using either vanilla JavaScript or jquery)
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Using jQuery, the textbox can be selected when it receives focus by calling the `.select()` method on the element.
---

**Contents**

[TOC]

### Vanilla JS

1. Add an event listener to the textbox element
```js
document.querySelector('#textbox').addEventListener('focus', function() {
    this.select();
});
```

2. Select all contents of textbox
```js
this.select();
```

### jQuery

1. Add an event listener to the textbox element
```js
$('#textbox').on('focus', function() {
    $(this).select();
});
```

2. Select all contents of textbox
```js
$(this).select();
```
