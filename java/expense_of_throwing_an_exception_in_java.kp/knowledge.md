---
title: What makes throwing an exception costly?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The actual creation and construction of the Exception object is the most expensive part of throwing an Exception in Java.
---

**Contents**

[TOC]

1. **Creating an Exception Object**
Creating an exception object requires constructing an object and storing it in memory. This can be expensive in terms of memory and time.

2. **Propagating the Exception**
Propagating the exception involves traversing the call stack and passing the exception object to each method on the stack. This can be expensive in terms of time and memory, as the exception must be passed from one method to the next.

3. **Handling the Exception**
Handling the exception requires the application to identify the exception, determine the appropriate response, and execute the response. This can be expensive in terms of time and resources, as the application must decide how to respond to the exception.

4. **Logging the Exception**
Logging the exception requires the application to record the exception in a log file or other persistent storage. This can be expensive in terms of time and resources, as the application must write the exception to the log file.
