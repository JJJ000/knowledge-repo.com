---
title: What is the method to include multiple statements on a single line?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can separate statements with a semicolon, but it is not recommended for readability purposes.
---

**Contents**

[TOC]

### Syntax

To put multiple statements in one line in Python, we can use a semicolon (;) to separate the statements. The syntax is as follows:

```python
statement1; statement2; statement3
```

Here, `statement1`, `statement2`, and `statement3` are the statements that we want to put in a single line.

### Example

Let's take an example where we want to print two strings on the same line:

```python
print("Hello, "); print("world!")
```

This will output:

```
Hello,
world!
```

Now, let's put these statements in a single line using semicolons:

```python
print("Hello, "); print("world!");
```

This will output:

```
Hello, world!
```

### Precautions

While using semicolons to put multiple statements in one line, we must be careful about the readability and maintainability of the code. The use of semicolons can make the code less readable and more difficult to maintain, especially when used excessively. Therefore, it is recommended to use semicolons only when it improves the readability and does not harm the maintainability of the code.
