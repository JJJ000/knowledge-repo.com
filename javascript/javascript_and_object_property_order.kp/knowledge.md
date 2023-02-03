---
title: Is the order of properties in JavaScript objects guaranteed?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: No, JavaScript does not guarantee object property order.
---

**Contents**

[TOC]

# No

JavaScript does not guarantee the order of object properties. The order of properties in an object can differ between engines and can even change when the object is modified.

# Why

The ECMAScript standard does not specify the order of properties in an object. Therefore, different JavaScript engines can implement the order differently, and even the same engine can change the order when the object is modified.

# Impact

This lack of guarantee can cause unexpected behavior if the order of properties is relied upon. It is best practice to not rely on the order of properties when working with objects in JavaScript.
