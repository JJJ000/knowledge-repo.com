---
title: What makes java's simpledateformat not thread-safe?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: SimpleDateFormat is not thread-safe because it is not immutable and multiple threads can access and modify the same instance of SimpleDateFormat.
---

**Contents**

[TOC]

1. Overview
---------------------
Java's SimpleDateFormat class is a class used to format and parse dates. It is not thread-safe, meaning that if multiple threads are accessing a single instance of the class, it can lead to unexpected results.

2. Reasons for Unsafe Threading
---------------------
The main reason for the lack of thread-safety in SimpleDateFormat is due to its use of mutable static fields. The static fields are used to store the current date and time, which are then used to format and parse dates. If multiple threads are accessing the same instance of SimpleDateFormat, they can overwrite each other's values, leading to unexpected results.

3. Possible Solutions
---------------------
The simplest solution to this problem is to use a thread-safe version of SimpleDateFormat such as ThreadLocalSimpleDateFormat. This version of the class uses thread-local variables to store the current date and time, meaning that each thread can have its own instance of the class and its own values for the static fields.

4. Conclusion
---------------------
Java's SimpleDateFormat is not thread-safe due to its use of mutable static fields. To avoid unexpected results, it is recommended to use a thread-safe version of the class such as ThreadLocalSimpleDateFormat.
