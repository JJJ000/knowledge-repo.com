---
title: What is the method to make pyflakes overlook a statement?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Add `# noqa` at the end of the line containing the statement to tell Pyflakes to ignore it.
---

**Contents**

[TOC]

## Introduction

Pyflakes is a Python library used for static code analysis. It analyses source code to identify and report any potential issues or errors. Pyflakes is useful in identifying issues like undefined variable names, unused imports, and more. In this post, we discuss how to get Pyflakes to ignore a statement in Python.

## Using #NOQA

The simplest way to tell Pyflakes to ignore a statement or line is to add `#NOQA` at the end of the statement. Here is an example:

```
name = 'John'
print(name)  #NOQA
```

Pyflakes will analyze the above code and ignore the `print(name)` statement.

## Using noqa

Another way to tell Pyflakes to ignore a statement or line is to add the `# noqa` tag at the end of the line. Here is an example:

```
name = 'John'
print(name)  # noqa
```

Pyflakes will also ignore the `print(name)` statement above.

## Using Flake8

Flake8 is a tool that combines several other linting tools, including Pyflakes. To tell Pyflakes to ignore a statement, you can use Flake8 by following the steps below:

1. Install Flake8 using pip:

```
pip install flake8
```

2. Create a `.flake8` file in your project's root directory

3. Add the following line to the `.flake8` file:

```
# flake8: noqa
```

With the above settings, Flake8 will ignore all Pyflakes errors in your codebase.

## Conclusion

Pyflakes is a great tool that can help you identify and fix potential issues in your Python code. However, in some cases, you may want to ignore some lines or statements. This post has shown you three ways to get Pyflakes to ignore a statement or line in Python.
