---
title: Create a basic html display
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: In JavaScript, you can use the innerHTML property of an element to render basic HTML view.
---

**Contents**

[TOC]

**Section 1 - Create the HTML Element**

```javascript
let view = document.createElement('div');
view.innerHTML = `
  <h1>Basic HTML View</h1>
  <p>This is a basic HTML view.</p>
`;
document.body.appendChild(view);
```

**Section 2 - Add Styles**

```javascript
view.style.width = '200px';
view.style.height = '200px';
view.style.backgroundColor = '#ccc';
view.style.padding = '10px';
```

**Section 3 - Add Classes**

```javascript
view.classList.add('basic-html-view');
```

**Section 4 - Add an ID**

```javascript
view.id = 'basic-html-view';
```
