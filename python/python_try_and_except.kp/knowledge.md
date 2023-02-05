---
title: Attempting multiple exceptions with python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Yes, you can use multiple except statements in a single try block.
---

**Contents**

[TOC]

# Section 1: Overview

Python allows you to use multiple exceptions in one try statement. This is a useful feature that enables you to handle different types of errors in a single try block. It also allows you to control the flow of execution in case of an error.

# Section 2: Syntax

The syntax for using multiple exceptions in one try statement is as follows:

```
try:
   # code block
except (Exception1, Exception2):
   # code block
```

The code block in the try statement will be executed first. If an exception is raised, the code in the except block will be executed.

# Section 3: Example

Here is an example of using multiple exceptions in one try statement:

```
try:
   # code block
except (TypeError, ValueError):
   # code block
```

In this example, the code block in the try statement will be executed first. If a TypeError or ValueError is raised, the code in the except block will be executed.

# Section 4: Benefits

Using multiple exceptions in one try statement has several benefits. It allows you to handle different types of errors in a single try block, which can make your code more efficient. It also allows you to control the flow of execution in case of an error.
