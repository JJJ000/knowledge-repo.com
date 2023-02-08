---
title: What steps can be taken to stop a form from being submitted?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Prevent form submission by using the event.preventDefault() method.
---

**Contents**

[TOC]

### Option 1: Return False

The most common way to prevent a form from being submitted is to return false in the `onsubmit` event handler of the form. This will stop the form from being submitted and any default actions that the browser may take.

```html
<form onsubmit="return false;">
    <!-- form elements -->
</form>
```

### Option 2: Prevent Default

Another way to prevent a form from being submitted is to call the `preventDefault()` method of the `event` object in the `onsubmit` event handler of the form. This will also stop the form from being submitted and any default actions that the browser may take.

```html
<form onsubmit="event.preventDefault();">
    <!-- form elements -->
</form>
```

### Option 3: Stop Propagation

A third way to prevent a form from being submitted is to call the `stopPropagation()` method of the `event` object in the `onsubmit` event handler of the form. This will stop the form from being submitted, but will not prevent any default actions that the browser may take.

```html
<form onsubmit="event.stopPropagation();">
    <!-- form elements -->
</form>
```

### Option 4: Return False and Prevent Default

A fourth way to prevent a form from being submitted is to return false and call the `preventDefault()` method of the `event` object in the `onsubmit` event handler of the form. This will stop the form from being submitted and any default actions that the browser may take.

```html
<form onsubmit="event.preventDefault(); return false;">
    <!-- form elements -->
</form>
```
