---
title: Verify if a user has reached the end of a certain element, not just the viewable area of the window
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can check if a user has scrolled to the bottom of an element by comparing the element`s scrollHeight and scrollTop properties with its clientHeight property.
---

**Contents**

[TOC]

### Solution

#### 1. Get the Element's Scroll Height

The first step is to get the scroll height of the element we want to check. This can be done by using the `scrollHeight` property on the element.

```javascript
const element = document.querySelector('#element');
const elementScrollHeight = element.scrollHeight;
```

#### 2. Get the Element's Scroll Position

We then need to get the current scroll position of the element. This can be done by using the `scrollTop` property.

```javascript
const elementScrollPosition = element.scrollTop;
```

#### 3. Calculate the Difference

We can then calculate the difference between the scroll height and the scroll position to determine how far the user has scrolled.

```javascript
const scrollDifference = elementScrollHeight - elementScrollPosition;
```

#### 4. Check if the User Has Scrolled to the Bottom

Finally, we can compare the difference to the element's height to determine if the user has scrolled to the bottom. If the difference is equal to or less than the element's height, then the user has scrolled to the bottom.

```javascript
const elementHeight = element.clientHeight;

if (scrollDifference <= elementHeight) {
  // User has scrolled to the bottom
}
```
