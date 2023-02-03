---
title: What are the contrasting effects of event.stoppropagation and event.preventdefault?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: event.stopPropagation prevents an event from bubbling up the event chain, while event.preventDefault prevents the default action of an event from being triggered.
---

**Contents**

[TOC]

### event.stopPropagation

event.stopPropagation is used to prevent an event from bubbling up the DOM tree, preventing any parent handlers from being notified of the event. It is most commonly used when dealing with events that propagate from a child element to a parent element.

### event.preventDefault

event.preventDefault is used to prevent the default action of an element from being triggered. This is most commonly used when dealing with form elements, such as a submit button, where the default action is to submit the form. It can also be used to prevent the default action of a link from being triggered, such as when a user clicks on a link and the browser navigates to the link’s destination.
