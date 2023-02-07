---
title: Avoid selecting text after double clicking
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Preventing text selection after a double click can be done by using the `onselectstart` event.
---

**Contents**

[TOC]

### Option 1: Disable Text Selection

This option uses the `onselectstart` event to disable text selection on the page.

```javascript
document.onselectstart = function () { return false; }
```

### Option 2: Disable Double Click

This option uses the `ondblclick` event to disable double click on the page.

```javascript
document.ondblclick = function () { return false; }
```

### Option 3: Use CSS

This option uses CSS to disable text selection on the page.

```css
body {
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
```

### Option 4: Use Unselectable Attribute

This option uses the `unselectable` attribute to disable text selection on the page.

```html
<div unselectable="on">
  This text cannot be selected.
</div>
```
