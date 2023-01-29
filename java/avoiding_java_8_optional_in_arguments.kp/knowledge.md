---
title: What are the drawbacks of using Java 8's optional in arguments?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Java 8`s Optional should not be used in arguments because it can lead to unnecessary complexity and confusion.
---

**Contents**

[TOC]

### Misconception of Functionality
Many developers mistakenly believe that Optional can be used to validate arguments. This is not the case. Optional is meant to be used to represent the presence or absence of a value, not to validate arguments.

### Unnecessary Complexity
Using Optional in arguments adds complexity to the codebase that is not necessary. It can also make code more difficult to read and understand.

### Limited Use Cases
Optional is only useful in certain circumstances and should not be used indiscriminately. It is not suited for all types of arguments and should only be used when it is absolutely necessary.

### Unnecessary Overhead
Using Optional in arguments adds unnecessary overhead to the codebase. This overhead can lead to slower performance and increased memory usage.
