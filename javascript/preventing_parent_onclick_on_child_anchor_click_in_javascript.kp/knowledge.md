---
title: What is the best way to stop a parent's onclick event from being triggered when a child anchor is clicked?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use event.stopPropagation() on the child anchor`s onclick event.
---

**Contents**

[TOC]

#### Event Bubbling

The most common way to prevent a parent's onclick event from firing when a child anchor is clicked is to use event bubbling. When an event is triggered on a DOM element, it will first run the handlers on it, then on its parent, then all the way up on other ancestors. Event bubbling allows us to stop the event from propagating to the ancestor elements by using the `event.stopPropagation()` method.

#### Using Event Delegation

Another way to prevent a parent's onclick event from firing when a child anchor is clicked is to use event delegation. This technique involves attaching a single event handler to a parent element, and then using logic inside the handler to target any descendants that match a given selector. This allows us to avoid attaching multiple event handlers to child elements, which can be more efficient.

#### Event Capturing

Another way to prevent a parent's onclick event from firing when a child anchor is clicked is to use event capturing. Event capturing is the opposite of event bubbling, where the event is first captured by the outermost element and propagates down to the inner elements. We can use the `event.stopPropagation()` method to prevent the event from propagating to the parent elements.

#### Event.stopImmediatePropagation()

Another way to prevent a parent's onclick event from firing when a child anchor is clicked is to use the `event.stopImmediatePropagation()` method. This method will stop the event from propagating to any of its parent elements and also prevent any other event handlers on the same element from running. This can be useful when there are multiple event handlers attached to a single element that need to be prevented from running.
