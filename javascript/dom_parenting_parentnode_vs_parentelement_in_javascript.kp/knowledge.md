---
title: What is the distinction between the dom parentnode and parentelement properties?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The parentNode property returns the parent node of the specified node, while the parentElement property returns the parent element of the specified node.
---

**Contents**

[TOC]

### parentNode

The parentNode property returns the parent node of the specified node, as a Node object.

### parentElement

The parentElement property returns the parent element of the specified element, as an Element object.

### Difference

The main difference between parentNode and parentElement is that parentNode returns the parent node as a Node object, while parentElement returns the parent element as an Element object. Additionally, parentNode will return the parent node of any node, while parentElement will only return the parent element of an Element node.
