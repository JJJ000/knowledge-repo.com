---
title: Locate the nearest parent element that has a particular class
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The closest ancestor element that has a specific class can be found by using the closest() method.
---

**Contents**

[TOC]

**Section 1: Finding the Element**

To find the closest ancestor element with a specific class in Javascript, the `closest()` method can be used. This method traverses up the DOM tree and finds the closest ancestor element that matches the selector.

**Section 2: Syntax**

The syntax for the `closest()` method is as follows:

```
element.closest(selector);
```

Where `element` is the element to search from and `selector` is the CSS selector to match the ancestor element.

**Section 3: Example**

For example, if we have the following HTML:

```
<div class="container">
  <div class="row">
    <div class="col-md-6">
      <div class="box">
        <div class="content">
          <p>Lorem ipsum dolor sit amet.</p>
        </div>
      </div>
    </div>
  </div>
</div>
```

And we want to find the closest ancestor element with the class `row`, we can use the following code:

```
const content = document.querySelector('.content');
const row = content.closest('.row');
```

**Section 4: Browser Support**

The `closest()` method is supported in all major browsers, including Chrome, Firefox, Edge, Safari, and IE11.
