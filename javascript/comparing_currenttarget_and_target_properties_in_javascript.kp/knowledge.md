---
title: What is the precise distinction between the currenttarget and target properties in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The currentTarget property refers to the element whose event listener triggered the event, whereas the target property refers to the element that triggered the event.
---

**Contents**

[TOC]

###CurrentTarget
CurrentTarget is the element to which the currently-called event handler has been attached. It's the element that the event handler is bound to.

###Target
Target is the element on which the event occurred. It's the element that initiated the event.
