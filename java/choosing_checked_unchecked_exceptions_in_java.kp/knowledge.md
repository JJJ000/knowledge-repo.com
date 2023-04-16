---
title: What are the differences between checked and unchecked exceptions?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Checked exceptions should be used for recoverable errors, such as invalid user input, while unchecked exceptions should be used for unrecoverable errors, such as programming bugs.
---

**Contents**

[TOC]

1. **Checked Exceptions**
   - Checked exceptions are those that the compiler checks for during compilation. They must be handled when using the throws clause or by using a try-catch block.
2. **Unchecked Exceptions**
   - Unchecked exceptions are those that the compiler does not check for during compilation. They are not required to be handled, but it is recommended to do so.
3. **When to Choose Checked Exceptions**
   - Checked exceptions should be used when the code needs to be able to handle the exception in a specific way, such as logging it or displaying an error message.
4. **When to Choose Unchecked Exceptions**
   - Unchecked exceptions should be used when the code does not need to handle the exception in a specific way, such as when the code is expected to fail and the user should be notified.
