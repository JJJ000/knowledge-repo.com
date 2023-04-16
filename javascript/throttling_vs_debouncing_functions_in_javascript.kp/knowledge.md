---
title: What is the distinction between limiting the frequency of a function's execution with throttling and delaying the execution of a function with debouncing?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Throttling limits the rate of a function`s triggered calls, while debouncing limits the rate of a function`s triggered calls to once after a certain period of time.
---

**Contents**

[TOC]

#Throttling
Throttling is a technique used to limit the number of times a function can be executed over a certain amount of time. It is used to limit the amount of resources consumed by a function, such as CPU or memory, and to ensure that a function does not run too often. Throttling works by setting a limit on the number of times a function can be called within a certain amount of time. If the limit is exceeded, the function will not be executed until the next time period.

#Debouncing
Debouncing is a technique used to delay the execution of a function until a certain amount of time has passed without it being called. It is used to ensure that a function is not called too frequently, such as when a user is typing in a text field. Debouncing works by setting a timer after a function is called, and if the function is called again before the timer expires, the timer is reset and the function is not executed until after the timer expires.

#Difference
The main difference between throttling and debouncing is that throttling limits the number of times a function can be executed within a certain amount of time, while debouncing delays the execution of a function until a certain amount of time has passed without it being called. Throttling is used to limit the amount of resources consumed by a function, while debouncing is used to ensure that a function is not called too frequently.
