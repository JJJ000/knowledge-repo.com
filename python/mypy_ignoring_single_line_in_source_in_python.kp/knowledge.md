---
title: In what way is it possible for mypy to exclude a specific line from a source file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Add a `# type ignore` comment at the end of the line.
---

**Contents**

[TOC]

Section 1: Background
Mypy is a static type checker for Python. It offers type annotation checking, type inference, and error detection services. Mypy catches many common errors in Python programs and offers a powerful tool for developers to improve code quality and maintainability. Sometimes, though, there are situations where it may be desirable to ignore certain lines of code when using mypy. This might be the case in situations where code is generated or where certain libraries are used that are not compatible with mypy.

Section 2: Using Annotations to Ignore Code
One way to ignore a single line in a source file in Python with mypy is to use annotations. Annotations are added to the code using comments or decorators. To ignore a line in a source file, the `# type: ignore` annotation can be added to that line. This tells mypy to skip checking that line of code.

For example:
```
# This line will be checked
x: int = 5
# This line will be ignored
y: str = "hello"  # type: ignore
```

In this example, mypy will check the first line and infer that `x` is an integer. It will ignore the second line entirely, treating `y` as an unannotated variable.

Section 3: Using Configuration Files to Ignore Code
Another way to ignore code in mypy is to use a configuration file. This approach is useful for cases where multiple files need to be ignored or where certain libraries need to be excluded from type checking.

In the configuration file, lines can be excluded using the `--ignore-errors` flag. This flag takes a list of error codes that should be ignored. In the case of ignoring a single line, the `ignore` code can be used.

For example, to ignore all `ignore` lines in the project, the following can be added to the configuration file:
```
[mypy]
ignore_errors = ignore
```

This will cause mypy to ignore any line in any file with the `# type: ignore` annotation.

Section 4: Conclusion
Mypy is a powerful tool for identifying type errors in Python code. However, there are situations where certain lines should be ignored. By adding annotations or configuring mypy using a configuration file, single lines or entire files can be excluded from type checking. Developers can use this feature to improve the quality and maintainability of their code while still maintaining flexibility and control.
