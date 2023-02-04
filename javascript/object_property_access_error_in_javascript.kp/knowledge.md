---
title: I am unable to retrieve the value of the object property, even though it appears in the console output
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Objects in JavaScript are passed by reference, so the value in the console log may not be up to date.
---

**Contents**

[TOC]

**Solution 1:**

Check the Scope
--------------------------------
If the property is showing up in the console log, it may be that the object is in the wrong scope. Make sure that the object is in the same scope as the code you are trying to access it from.

**Solution 2:**

Check the Syntax
--------------------------------
Make sure that the syntax you are using to access the property is correct. For example, if the object is stored in a variable, make sure you are using the correct syntax for accessing the property: `variable.property`.
