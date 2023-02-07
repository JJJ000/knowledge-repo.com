---
title: What is the distinction between the $observe and $watch methods in angularjs?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The $observe method is used to observe changes to an AngularJS expression, while the $watch method is used to watch changes to a scope variable.
---

**Contents**

[TOC]

### $observe

$observe is a method used to observe the changes in an expression. It is called whenever the value of the expression changes. It also supports deep watching of the expression.

### $watch

$watch is a method used to watch the changes in a scope variable. It is called whenever the value of the scope variable changes. It does not support deep watching.
