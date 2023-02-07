---
title: What is the distinction between textcontent and innertext?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: textContent returns the full text content of a given element, including all child elements, while innerText only returns the visible text content of a given element.
---

**Contents**

[TOC]

## textContent
textContent is a property of a DOM element that returns the text content of the element. It does not include the text of any of the element's descendants.

## innerText
innerText is a property of a DOM element that returns the text content of the element, including the text of any of the element's descendants.

## Difference
The main difference between textContent and innerText is that textContent returns the text content of the element, while innerText returns the text content of the element, including the text of any of the element's descendants. Additionally, innerText takes into account the styling of the text, while textContent does not.
