---
title: What is the jquery code to determine the absolute position of an element?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the jQuery .offset() method to find the absolute position of an element.
---

**Contents**

[TOC]

# Section 1: Finding the Position of an Element

The jQuery `position()` method can be used to find the absolute position of an element relative to its offset parent.

# Section 2: Using the Position Method

To use the `position()` method, the syntax is `$(selector).position()`. This will return an object containing the properties `top` and `left`, which represent the number of pixels the element is from the left and top of its offset parent.

# Section 3: Example

For example, if you wanted to find the absolute position of an element with the id `myButton`, you could use the following code:

```javascript
var position = $("#myButton").position();
```

# Section 4: Accessing the Position

Once the position has been retrieved, you can access the `top` and `left` properties to get the absolute position of the element. For example, if you wanted to get the number of pixels from the left edge of the offset parent, you could use the following code:

```javascript
var left = position.left;
```
