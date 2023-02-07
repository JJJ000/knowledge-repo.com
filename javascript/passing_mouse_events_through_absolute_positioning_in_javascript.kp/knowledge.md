---
title: Send mouse events through an element that has an absolute positioning
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Passing mouse events through an absolutely-positioned element can be done by setting the element`s `pointer-events` property to `none`.
---

**Contents**

[TOC]

#### Event Capturing

Mouse events can be passed through an absolutely-positioned element in Javascript by using event capturing. Event capturing is a process in which an event propagates through the DOM tree from its target element to the top of the DOM tree. When an event is captured, the capturing element can be used to pass the event to the next element in the DOM tree. 

#### Event Bubbling

Event bubbling is the opposite of event capturing. It is a process in which an event propagates from the top of the DOM tree to its target element. When an event is bubbled, the bubbling element can be used to pass the event to the next element in the DOM tree.

#### Event Listeners

Event listeners can be used to listen for mouse events on an absolutely-positioned element. The event listener can be used to detect when a mouse event has occurred and then pass the event to the next element in the DOM tree.

#### Event Propagation

Event propagation is the process of passing an event from one element to another. Event propagation can be used to pass mouse events through an absolutely-positioned element in Javascript. Event propagation can be used to pass the event to the next element in the DOM tree.
