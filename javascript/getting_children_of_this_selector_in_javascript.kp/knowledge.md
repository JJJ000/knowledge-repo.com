---
title: What is the syntax for retrieving the descendants of the $(this) selector?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the $(this).children() method to get the children of the $(this) selector.
---

**Contents**

[TOC]

1. Using the `children()` Method 

The `children()` method can be used to get the children of the `$(this)` selector in Javascript. It will return all direct children of the selected element.

2. Example

Here is an example of how to use the `children()` method to get the children of the `$(this)` selector:

```javascript
$(this).children().each(function(){
    // Do something with each child element
});
```

3. Using the `find()` Method 

The `find()` method can also be used to get the children of the `$(this)` selector in Javascript. It will return all descendants of the selected element, not just direct children.

4. Example

Here is an example of how to use the `find()` method to get the children of the `$(this)` selector:

```javascript
$(this).find('*').each(function(){
    // Do something with each descendant element
});
```
