---
title: Adjusting the position of an html anchor to account for a fixed header
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Offsetting an HTML anchor can be done by adding an offset to the anchor`s scrollTop position when the page is scrolled.
---

**Contents**

[TOC]

**Section 1: Overview**

Offsetting an HTML anchor is a technique used to adjust the position of an anchor element on a page when a fixed header is present. This is done by using JavaScript to calculate the height of the fixed header and then offsetting the anchor by that amount. This ensures that when a user clicks on the anchor, the content that the anchor is pointing to will appear at the top of the page, rather than being obscured by the fixed header.

**Section 2: Calculating the Offset Amount**

The first step in offsetting an HTML anchor is to calculate the amount that needs to be offset. This can be done by using JavaScript to get the height of the fixed header, then subtracting that value from the total height of the page. The result of this calculation will be the amount that needs to be offset in order to ensure that the content that the anchor is pointing to appears at the top of the page.

**Section 3: Applying the Offset**

Once the offset amount has been calculated, the next step is to apply the offset to the anchor. This can be done by using JavaScript to set the anchor's `top` property to the offset amount. This will ensure that when the anchor is clicked, the content that it is pointing to will appear at the top of the page, rather than being obscured by the fixed header.

**Section 4: Example Code**

Below is an example of how to offset an HTML anchor to adjust for a fixed header using JavaScript:

```javascript
// Get the height of the fixed header
var headerHeight = document.querySelector(".fixed-header").offsetHeight;

// Calculate the offset amount
var offsetAmount = window.innerHeight - headerHeight;

// Apply the offset to the anchor
document.querySelector("#anchor").style.top = offsetAmount + "px";
```
