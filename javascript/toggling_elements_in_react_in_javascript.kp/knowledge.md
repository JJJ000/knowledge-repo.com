---
title: Toggle visibility of an element in react
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: To show or hide an element in React, use the ternary operator or the JavaScript conditional operator to set the element`s display property to either `block` or `none`.
---

**Contents**

[TOC]

**Section 1: Show Element**

To show an element in React, use the `setState` method to update the state of the component and set the `display` property of the element to `block`:

```js
this.setState({
  display: "block"
});
```

**Section 2: Hide Element**

To hide an element in React, use the `setState` method to update the state of the component and set the `display` property of the element to `none`:

```js
this.setState({
  display: "none"
});
```

**Section 3: Using `style` Property**

Alternatively, you can use the `style` property to show or hide an element in React. To show an element, set the `display` property of the `style` object to `block`:

```js
<div style={{ display: "block" }}>
  This element is visible.
</div>
```

To hide an element, set the `display` property of the `style` object to `none`:

```js
<div style={{ display: "none" }}>
  This element is hidden.
</div>
```

**Section 4: Using `className` Property**

You can also use the `className` property to show or hide an element in React. To show an element, set the `className` property to a class that sets the `display` property to `block`:

```js
<div className="visible">
  This element is visible.
</div>
```

```css
.visible {
  display: block;
}
```

To hide an element, set the `className` property to a class that sets the `display` property to `none`:

```js
<div className="hidden">
  This element is hidden.
</div>
```

```css
.hidden {
  display: none;
}
```
