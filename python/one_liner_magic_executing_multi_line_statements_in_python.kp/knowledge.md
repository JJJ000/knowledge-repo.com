---
title: Performing one-line commands with multiple lines of code
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use semicolons to separate the statements, for example print(`Hello`);print(`World`) will print `Hello` and `World` on separate lines.
---

**Contents**

[TOC]

Section 1: Introduction

Python provides a way to execute code directly in the command-line interface using the one-line command-line. This is useful for quickly testing small pieces of code or running certain tasks. However, when you need to execute multi-line statements, the one-line command-line may not be enough. In this article, we will explore ways to execute multi-line statements in the one-line command-line in Python.

Section 2: Using a backslash to continue statements

One way to execute multi-line statements in the one-line command-line in Python is by using a backslash (\) to continue the statement on the next line. For example:

```
>>> print("Hello World! \
... This is a multi-line statement \
... using a backslash.")
Hello World! This is a multi-line statement using a backslash.
```

In the above example, we used the backslash (\) to continue the statement on the next line, allowing us to write multiple lines of code in the one-line command-line.

Section 3: Using parenthesis to group statements

Another way to execute multi-line statements in the one-line command-line in Python is by using parenthesis to group statements. For example:

```
>>> print("Hello World!"
...       "This is a multi-line statement "
...       "using parenthesis.")
Hello World!This is a multi-line statement using parenthesis.
```

In the above example, we used parenthesis to group the different parts of the statement, allowing us to write multiple lines of code in the one-line command-line.

Section 4: Using the semicolon operator to separate statements

Finally, we can use the semicolon operator (;) to separate statements in the one-line command-line in Python. For example:

```
>>> print("Hello World!"); print("This is a multi-line statement"); print("using a semicolon.")
Hello World!
This is a multi-line statement
using a semicolon.
```

In the above example, we used the semicolon operator (;) to separate the different parts of the statement, allowing us to write multiple lines of code in the one-line command-line.

Section 5: Conclusion

In this article, we explored ways to execute multi-line statements in the one-line command-line in Python. We can use a backslash to continue statements, parenthesis to group statements, or the semicolon operator to separate statements. These techniques allow us to write multiple lines of code in the one-line command-line, making it more versatile for testing and running tasks.
