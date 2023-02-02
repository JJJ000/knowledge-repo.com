---
title: Use jquery to move to a specific element on the page
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: $(`element`).scrollIntoView();
---

**Contents**

[TOC]

**Section 1: Selecting the Element**

To scroll to an element using jQuery, the first step is to select the element. This can be done using jQuery's `$()` selector function. For example, if the element has an ID of "myElement", the following code can be used to select it:

```javascript
var myElement = $('#myElement');
```

**Section 2: Calculating the Scroll Position**

Once the element is selected, the next step is to calculate the scroll position of the element. This can be done by using jQuery's `offset()` function. This will return an object containing the element's position relative to the document.

```javascript
var elementPosition = myElement.offset();
```

**Section 3: Scrolling to the Element**

Once the element's position is known, the final step is to scroll to the element. This can be done by using jQuery's `scrollTop()` function. This function takes a number as an argument, which is the number of pixels to scroll.

```javascript
$('html, body').scrollTop(elementPosition.top);
```

**Section 4: Finishing Up**

Once the element is scrolled to, the process is complete. To finish up, it's a good idea to add a callback function that will be executed once the scrolling is finished. This can be done by passing a function as an argument to the `scrollTop()` function.

```javascript
$('html, body').scrollTop(elementPosition.top, function() {
  // Code to run after scrolling is finished
});
```
