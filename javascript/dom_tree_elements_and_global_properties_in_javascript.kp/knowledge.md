---
title: Are dom tree elements with ids converted into global properties?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: No, DOM tree elements with IDs do not become global properties in Javascript.
---

**Contents**

[TOC]

##No
DOM tree elements with IDs do not become global properties in Javascript. 

##How IDs Work
IDs are used to identify a specific element in the DOM tree. When an element is identified with an ID, the browser creates a global variable with the same name as the ID. This variable points to the element in the DOM tree. 

##Why Not Global Properties
However, this does not mean that the DOM tree elements with IDs become global properties in Javascript. The variables created by the browser are not global properties, they are simply variables that point to the element in the DOM tree. The variables can be used to access and manipulate the element, but they are not global properties. 

##Conclusion
In conclusion, DOM tree elements with IDs do not become global properties in Javascript. The browser creates a variable with the same name as the ID, but this variable is not a global property. It is simply a variable that points to the element in the DOM tree.
