---
title: What is the syntax to exit out of a jquery each() function?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the `return false` statement within the each() function to break/exit from it.
---

**Contents**

[TOC]

# Solution 1: 
Returning False

The most common way to break out of a `each()` loop is to use the `return false` statement inside the loop. This will immediately stop the loop from further execution.

# Solution 2: 
Using a Boolean Variable

Another way to break out of a `each()` loop is to use a boolean variable. Set the boolean variable to `true` when you want to break out of the loop. In the loop, check the boolean variable and break out of the loop if it is `true`.

# Solution 3:
Using a Label

A third way to break out of a `each()` loop is to use a label. Labels are used to identify a block of code. You can use the `break` statement with a label to break out of the loop.

# Solution 4:
Using a Counter

The fourth way to break out of a `each()` loop is to use a counter. Set the counter to a certain value when you want to break out of the loop. In the loop, check the counter and break out of the loop if it reaches the desired value.
