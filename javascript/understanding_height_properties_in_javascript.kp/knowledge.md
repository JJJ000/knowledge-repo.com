---
title: What do offsetheight, clientheight, and scrollheight refer to?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: OffsetHeight is the height of an element including padding, clientHeight is the height of an element excluding padding and scrollHeight is the total height of an element including padding and scrollable content.
---

**Contents**

[TOC]

## offsetHeight
The offsetHeight property returns the viewable height of an element in pixels, including padding, border and scrollbar, but not the margin.

## clientHeight
The clientHeight property returns the viewable height of an element in pixels, including padding, but not the border, scrollbar or margin.

## scrollHeight
The scrollHeight property returns the total height of an element in pixels, including padding, border and scrollbar, but not the margin.

## Difference
The main difference between offsetHeight, clientHeight and scrollHeight is that offsetHeight includes the element's border, whereas clientHeight does not. scrollHeight includes the element's padding, border and scrollbar, whereas the other two do not.
