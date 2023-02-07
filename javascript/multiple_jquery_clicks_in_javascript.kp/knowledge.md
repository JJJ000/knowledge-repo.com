---
title: Jquery click events triggering multiple times
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: To prevent jQuery click events from firing multiple times, use event.stopPropagation() or return false.
---

**Contents**

[TOC]

1. Overview

jQuery click events can sometimes fire multiple times when triggered by a Javascript function. This can be due to a variety of factors, including incorrect event delegation, lack of event delegation, or incorrect event binding.

2. Incorrect Event Delegation

When an event is delegated incorrectly, it can cause the event to fire multiple times. For example, if an event is delegated to a parent element, but the element that the event is triggered on is a child element, then the event will fire multiple times. This is because the parent element will receive the event and trigger it multiple times.

3. Lack of Event Delegation

When an event is not delegated, it can also cause the event to fire multiple times. This is because the event will be triggered on all elements that match the selector, instead of just the element that the event was intended to be triggered on.

4. Incorrect Event Binding

Incorrect event binding can also cause an event to fire multiple times. This is because the event will be bound to multiple elements, instead of just one. This can happen if the selector is too broad, or if the event is bound to an element that has already been bound to the event.
