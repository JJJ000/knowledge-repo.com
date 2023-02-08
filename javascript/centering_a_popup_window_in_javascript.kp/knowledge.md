---
title: How can I position a popup window in the middle of the screen?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the window.open() method with the `top` and `left` parameters set to the center of the screen.
---

**Contents**

[TOC]

1. Get the Screen Dimensions
2. Calculate the Popup Window Position
3. Set the Popup Window Position
4. Test the Result

#### 1. Get the Screen Dimensions

We need to get the size of the user's screen in order to calculate the position of the popup window. This can be done using the `window.screen` object.

```javascript
const screenWidth = window.screen.width;
const screenHeight = window.screen.height;
```

#### 2. Calculate the Popup Window Position

Now that we have the screen dimensions, we can calculate the position of the popup window. We need to take into account the size of the popup window as well as the user's screen size.

```javascript
const popupWidth = 500;
const popupHeight = 400;

const left = (screenWidth - popupWidth) / 2;
const top = (screenHeight - popupHeight) / 2;
```

#### 3. Set the Popup Window Position

Now that we have the position of the popup window, we can set it using the `window.open()` method.

```javascript
window.open('popup.html', 'Popup Window', `left=${left},top=${top},width=${popupWidth},height=${popupHeight}`);
```

#### 4. Test the Result

Finally, we can test the result by opening the popup window and ensuring it is centered on the screen.
