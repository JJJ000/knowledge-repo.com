---
title: What is the process for accessing evaluated attributes within a custom directive?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The evaluated attributes can be accessed inside a custom directive by using the $attrs service.
---

**Contents**

[TOC]

1.  Using `$scope`

The `$scope` object is the most commonly used method to get evaluated attributes inside a custom directive. The `$scope` object provides access to the scope of the directive, allowing you to get the evaluated attributes as properties. 

2. Using `$attrs`

The `$attrs` object is another method to get evaluated attributes inside a custom directive. The `$attrs` object provides access to the attributes of the directive, allowing you to get the evaluated attributes as properties. 

3. Using `$eval`

The `$eval` function is a method to evaluate an expression in the context of the scope of the directive. The `$eval` function can be used to evaluate the attributes of the directive, allowing you to get the evaluated attributes as properties. 

4. Using `$parse`

The `$parse` function is a method to parse an expression in the context of the scope of the directive. The `$parse` function can be used to parse the attributes of the directive, allowing you to get the evaluated attributes as properties.
