---
title: What is the process for turning off html links?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: HTML links can be disabled in Javascript by using the `pointer-events none` CSS property.
---

**Contents**

[TOC]

# Section 1: Using CSS

You can use the CSS `pointer-events` property to disable HTML links. This property is set to `none` to disable the link, like so:

```css
a { 
  pointer-events: none;
}
```

# Section 2: Using JavaScript

You can also use JavaScript to disable HTML links. This can be done by adding an `onclick` event handler to the `a` element and then returning `false` from the handler.

```html
<a href="http://example.com" onclick="return false;">Example Link</a>
```

# Section 3: Using jQuery

If you are using jQuery, you can use the `.off()` method to disable HTML links. This method will remove all event handlers from the element, including the `onclick` handler.

```js
$('a').off('click');
```

# Section 4: Using HTML

Finally, you can also use the HTML `disabled` attribute to disable HTML links. This attribute will prevent the link from being clicked or focused.

```html
<a href="http://example.com" disabled>Example Link</a>
```
