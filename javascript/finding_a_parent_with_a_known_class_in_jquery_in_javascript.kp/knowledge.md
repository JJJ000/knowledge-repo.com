---
title: What is the syntax to locate a parent element with a specific class using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the jQuery selector `$(`.className`)` to find a parent with a known class.
---

**Contents**

[TOC]

**Section 1: Using the Parent Selector**

The parent selector can be used to find a parent element with a known class in jQuery. The syntax for this selector is `$(selector).parent('.className')`. This selector will traverse up the DOM tree until the parent element with the specified class name is found.

**Section 2: Using the Closest Selector**

The closest selector can also be used to find a parent element with a known class in jQuery. The syntax for this selector is `$(selector).closest('.className')`. This selector will traverse up the DOM tree until the closest parent element with the specified class name is found.

**Section 3: Using the Parents Selector**

The parents selector can also be used to find a parent element with a known class in jQuery. The syntax for this selector is `$(selector).parents('.className')`. This selector will traverse up the DOM tree and return all parent elements with the specified class name.

**Section 4: Using the Ancestors Selector**

The ancestors selector can also be used to find a parent element with a known class in jQuery. The syntax for this selector is `$(selector).ancestors('.className')`. This selector will traverse up the DOM tree and return all ancestor elements with the specified class name.
