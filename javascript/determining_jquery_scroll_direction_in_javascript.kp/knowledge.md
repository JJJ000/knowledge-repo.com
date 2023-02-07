---
title: What is the method for figuring out the direction of a jquery scroll event?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The direction of a jQuery scroll event can be determined by checking the value of the scrollTop or scrollLeft properties.
---

**Contents**

[TOC]

1. **Determine the Scroll Direction**

The easiest way to determine the direction of a jQuery scroll event is to use the `scrollTop()` method. This method returns the vertical scrollbar position of the element. By comparing the current scrollbar position with the previous scrollbar position, you can determine the direction of the scroll.

2. **Create Variables to Track Scroll Position**

First, you need to create two variables to store the current and previous scrollbar positions. You can use `let` or `var` to declare these variables.

3. **Use the ScrollTop() Method**

Next, use the `scrollTop()` method to get the current scrollbar position. Store this value in the variable you created in the previous step.

4. **Compare the Values**

Finally, compare the current and previous scrollbar positions. If the current scrollbar position is greater than the previous scrollbar position, then the scroll is going down. If the current scrollbar position is less than the previous scrollbar position, then the scroll is going up.
