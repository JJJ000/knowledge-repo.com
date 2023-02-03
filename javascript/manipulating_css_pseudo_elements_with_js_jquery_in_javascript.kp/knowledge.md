---
title: Using JavaScript (or jquery), selecting and altering css pseudo-elements such as before and after
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Using jQuery, it is possible to select and manipulate CSS pseudo-elements such as before and after using the .css() method.
---

**Contents**

[TOC]

**Creating a Pseudo-Element with Javascript**

Pseudo-elements can be created with the `document.createElement()` method. The syntax for creating a pseudo-element is as follows:

```
let pseudoElement = document.createElement('::before');
```

**Selecting a Pseudo-Element with Javascript**

Pseudo-elements can be selected with the `document.querySelector()` method. The syntax for selecting a pseudo-element is as follows:

```
let pseudoElement = document.querySelector('::before');
```

**Manipulating a Pseudo-Element with Javascript**

Pseudo-elements can be manipulated with the `style` property. The syntax for manipulating a pseudo-element is as follows:

```
pseudoElement.style.backgroundColor = '#000000';
```

**Manipulating a Pseudo-Element with jQuery**

Pseudo-elements can also be manipulated with jQuery. The syntax for manipulating a pseudo-element with jQuery is as follows:

```
$('::before').css('background-color', '#000000');
```
