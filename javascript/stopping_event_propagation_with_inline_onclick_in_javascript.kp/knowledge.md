---
title: What is the best way to prevent an event from bubbling up the dom when using an inline onclick attribute?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `event.stopPropagation()` method in the onclick attribute.
---

**Contents**

[TOC]

## Using Event.stopPropagation()

The `event.stopPropagation()` method is used to stop the bubbling of an event to parent elements, preventing any parent event handlers from being executed. This can be used with the `onclick` attribute in an inline event handler.

```html
<div onclick="event.stopPropagation();">
  <!-- Content -->
</div>
```

## Using Return False

The `return false` statement is another way to stop the propagation of an event. It is often used in jQuery event handlers, but can also be used in the `onclick` attribute of an HTML element.

```html
<div onclick="return false;">
  <!-- Content -->
</div>
```

## Using Event.stopImmediatePropagation()

The `event.stopImmediatePropagation()` method is similar to `event.stopPropagation()`, but it will also prevent any other event handlers from being executed. This can be used with the `onclick` attribute in an inline event handler.

```html
<div onclick="event.stopImmediatePropagation();">
  <!-- Content -->
</div>
```

## Using Event.preventDefault()

The `event.preventDefault()` method is used to prevent the default action of an event from being triggered. This can be used with the `onclick` attribute in an inline event handler.

```html
<div onclick="event.preventDefault();">
  <!-- Content -->
</div>
```
