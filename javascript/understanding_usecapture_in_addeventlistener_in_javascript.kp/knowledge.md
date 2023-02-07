---
title: What does the usecapture parameter in addeventlistener do?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The useCapture parameter determines whether the event should be handled by the capturing phase or the bubbling phase.
---

**Contents**

[TOC]

1. What is the useCapture Parameter?
The useCapture parameter is an optional parameter used in the addEventListener() method. It is a Boolean value that determines whether the event should be executed in the capturing or bubbling phase.

2. Capturing and Bubbling
Capturing is the process of capturing the event from the top down. The event is first captured by the outermost element and then propagates down to the inner elements. Bubbling is the opposite process, where the event is first captured by the innermost element and then propagates up to the outer elements.

3. When to Use the useCapture Parameter
The useCapture parameter is used when the event should be executed in the capturing phase. This is useful when the event should be executed on the outermost element first, and then propagates inward.

4. Default Value
The default value of the useCapture parameter is false, which means that the event will be executed in the bubbling phase.
