---
title: Angular window resizing event
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The window resize event in Angular can be handled by subscribing to the fromEvent() observable in the Angular HostListener.
---

**Contents**

[TOC]

### Section 1: Setting up the Event Handler

In order to capture the window resize event in Angular, you will need to set up an event handler. This can be done by using the `@HostListener` decorator.

### Section 2: Using the Event Handler

Once the event handler is set up, you can use it to capture the window resize event. To do this, you will need to pass the `'window:resize'` string as an argument to the `@HostListener` decorator.

### Section 3: Handling the Event

Once the window resize event is captured, you will need to handle it. You can do this by defining a function that will be called when the window is resized. This function can contain any logic you need to execute when the window is resized.

### Section 4: Using the Data

Once the window resize event is handled, you can use the data from the event to take any necessary action. For example, you can use the data to adjust the size of elements on the page or to update the layout of the page.
