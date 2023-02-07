---
title: The difference between stoppropagation and stopimmediatepropagation is that stoppropagation prevents further propagation of the current event in the capturing and bubbling phases, while stopimmediatepropagation prevents further propagation of the current event in the capturing, bubbling and any other event listeners that may be attached
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: stopPropagation prevents further bubbling of the event, while stopImmediatePropagation prevents further bubbling and stops any other handlers from being called.
---

**Contents**

[TOC]

## stopPropagation

stopPropagation() is a method in Javascript that stops the bubbling of an event to parent elements, but does not stop other listeners on the same element from being executed.

## stopImmediatePropagation

stopImmediatePropagation() is a method in Javascript that stops the bubbling of an event to parent elements, as well as prevents any other listeners on the same element from being executed.

## Difference

The main difference between stopPropagation and stopImmediatePropagation is that stopImmediatePropagation prevents any other listeners on the same element from being executed, while stopPropagation does not.
