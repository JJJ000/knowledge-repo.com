---
title: How do children and childnodes differ in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: ChildNodes includes all elements, including text and comment nodes, while children only includes element nodes.
---

**Contents**

[TOC]

### Definition

Children: The children property returns a collection of an element's child elements, as an HTMLCollection object.

ChildNodes: The childNodes property returns a collection of an element's child nodes, as a NodeList object.

### Difference

1. **Type:** Children returns an HTMLCollection object, while childNodes returns a NodeList object. 
2. **Including Text Nodes:** ChildNodes includes text nodes, while children does not. 
3. **Indexing:** Children can be accessed by index numbers, while childNodes can be accessed by index numbers or node types. 
4. **Live vs. Static:** Children is a live collection, meaning that it updates automatically when the document is changed, while childNodes is a static collection, meaning that it does not update automatically when the document is changed.
