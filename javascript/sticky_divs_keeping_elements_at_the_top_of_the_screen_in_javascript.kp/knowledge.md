---
title: Once a div has been scrolled to, what is the best way to keep it at the top of the screen?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the `position sticky` CSS property to make a div stick to the top of the screen once it has been scrolled to.
---

**Contents**

[TOC]

**Section 1: Add a CSS Class**

First, add a class to the div that you want to stick to the top of the screen. For example, if the div has an id of "sticky-div", you can add a class of "sticky-div-top" to it.

**Section 2: Add Event Listeners**

Next, add event listeners to the window object to detect when the user scrolls the page. This can be done using the `scroll` event.

**Section 3: Update the CSS Class**

When the user scrolls the page, update the class of the div to make it stick to the top of the screen. This can be done using the `top` property of the CSS.

**Section 4: Update the Position**

Finally, update the position of the div when the user scrolls the page. This can be done using the `position` property of the CSS. Set the position to `fixed` to make the div stick to the top of the screen.
