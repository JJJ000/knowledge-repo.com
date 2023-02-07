---
title: How can I use chrome developer tools to identify the code associated with a button or element?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Using the Developer Tools in Chrome, you can right-click on the button or element and select `Inspect` to view the associated Javascript code.
---

**Contents**

[TOC]

## Inspect Element 
1. Right-click the element on the page you want to inspect.
2. Select "Inspect" from the context menu. 
3. The Developer Tools pane will open at the bottom of the page.

## Locate the Code 
1. Select the "Elements" tab in the Developer Tools pane. 
2. Expand the HTML tree in the pane to locate the code associated with the element.
3. The code associated with the element will be highlighted in the pane.

## Analyze the Code 
1. Read the code associated with the element to determine which JavaScript functions are called when the element is clicked. 
2. Look for any event handlers that are attached to the element.
3. If the element has an event handler, look for the function call associated with it.

## Test the Code 
1. Select the "Sources" tab in the Developer Tools pane. 
2. Locate the function associated with the event handler in the Sources pane. 
3. Right-click the function and select "Break on > Next" to set a breakpoint. 
4. Click the element on the page to trigger the event handler. 
5. The debugger will pause at the breakpoint, allowing you to step through the code and analyze how it works.
