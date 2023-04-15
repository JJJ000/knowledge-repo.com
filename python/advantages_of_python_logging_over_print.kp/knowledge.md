---
title: What is the reason for using logging instead of print in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Logging allows for more granular control over the level, format, and destination of log messages.
---

**Contents**

[TOC]

## 1. Better control over output
Using print statements in code is a common way to debug and understand what is happening. However, it can be difficult to filter relevant output in large codebases or production environments. By using a logging library, you gain better control over what gets output and where it goes. You can set different logging levels to only output critical errors, for example, or send logs to a file instead of printing to the console.


## 2. Maintainability
When using print statements, it can be easy to forget to remove them after debugging, leading to unnecessary output in production code. Additionally, print statements may not conform to a consistent format, making it harder to compare outputs from different parts of the codebase. With logging, you can define a consistent format for your logs and disable or remove them easily when they are no longer needed.


## 3. Performance
While print statements are a convenient way to output information during development, they can be slower than logging in production code. This is because logging libraries often utilize buffering and other optimizations to improve performance. Additionally, logging can be configured to only output logs that meet certain criteria, reducing the amount of unnecessary output that the program has to process.


## Conclusion
While print statements can be useful in small codebases or during development, logging provides better control, maintainability, and performance, making it a better choice for production code. By using logging, you can easily configure and filter output, ensuring that you only see what is relevant and necessary.
