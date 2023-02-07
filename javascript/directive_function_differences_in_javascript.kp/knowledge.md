---
title: The 'controller' function is used to create a controller for a directive, which can be used to interact with the directive's template. the 'link' function is used to manipulate the dom, and the 'compile' function is used to allow the directive to modify the template before it is rendered
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The `controller` function defines the behavior of the directive, the `link` function allows us to manipulate the DOM, and the `compile` function allows us to modify the template before it is linked to the directive.
---

**Contents**

[TOC]

#### Controller
The controller function of a directive is used to create a controller for the directive. It is invoked when the directive is compiled and instantiated. It is responsible for setting up the scope and providing the data that will be used in the directive's template.

#### Link
The link function of a directive is used to register DOM listeners as well as update the DOM. It is invoked after the directive's template has been cloned and the scope has been initialized. It is responsible for manipulating the DOM elements and responding to DOM events.

#### Compile
The compile function of a directive is used to change the template before it is cloned. It is invoked before the link function and is responsible for manipulating the template DOM. It is used to create reusable components and optimize the performance of the directive.
