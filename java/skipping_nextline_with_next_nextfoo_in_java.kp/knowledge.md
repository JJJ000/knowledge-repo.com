---
title: Is the scanner not progressing to the next line after using next() or nextfoo()?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: This is because next() and nextFoo() methods do not read the newline character after the input given by the user, so the nextLine() method is left waiting for an input.
---

**Contents**

[TOC]

### Overview
When using a Scanner object in Java, it is possible for the Scanner to skip over the nextLine() method after using the next(), nextFoo(), or other methods. This can cause unexpected behavior in code, leading to errors or incorrect results. In this answer, we will discuss the cause of this behavior and how it can be avoided.

### Cause
The cause of this behavior is the fact that the Scanner's next() and nextFoo() methods do not consume the newline character that is left in the input stream after the user inputs their data. As a result, when the nextLine() method is called, the newline character is the first thing it reads, causing it to skip over the actual line of input.

### Workaround
One way to avoid this behavior is to use the Scanner's nextLine() method before using the other methods. This will consume the newline character, allowing the nextLine() method to read the actual line of input.

### Conclusion
When using a Scanner object in Java, it is important to be aware of the behavior of the Scanner's next() and nextFoo() methods. These methods do not consume the newline character that is left in the input stream, which can cause the nextLine() method to skip over the actual line of input. To avoid this behavior, the Scanner's nextLine() method should be used before using the other methods.
