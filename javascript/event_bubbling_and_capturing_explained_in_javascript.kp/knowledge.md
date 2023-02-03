---
title: What are the concepts of event bubbling and capturing?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Event bubbling and capturing are two methods of event propagation in the HTML DOM, where an event on an element can propagate to its parent or child elements.
---

**Contents**

[TOC]

#### Event Bubbling
Event bubbling is a concept in which an event in a child element propagates to its parent element and continues to propagate up the DOM tree. This is the opposite of event capturing, which propagates an event from the top of the DOM tree to the target element.

#### Event Capturing
Event capturing is a concept in which an event in a parent element propagates to its child element and continues to propagate down the DOM tree. This is the opposite of event bubbling, which propagates an event from the target element to the top of the DOM tree.

#### Event Bubbling vs Event Capturing
Event bubbling and event capturing are two different ways of propagating an event in the DOM tree. Event bubbling starts at the target element and propagates up the DOM tree, while event capturing starts at the top of the DOM tree and propagates down to the target element.

#### Browser Support
Event bubbling and event capturing are supported by all major browsers, including Chrome, Firefox, Safari, and Edge.
