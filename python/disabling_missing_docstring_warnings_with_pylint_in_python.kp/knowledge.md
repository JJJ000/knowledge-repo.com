---
title: What is the method to turn off pylint's "missing docstring" alerts for an entire file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Add `# pylint disable=missing-docstring` at the top of the Python file.
---

**Contents**

[TOC]

### Introduction
Pylint is a popular code analysis tool for Python. It is widely used to identify and report errors and warnings in Python code. This tool has a set of rules which are used to evaluate the quality of the code. One of the rules is to check for missing docstrings in a file. When you run Pylint on your Python code, it may produce warnings when it detects that some files are missing docstrings. 

In some cases, you may want to disable these warnings. This article explains how to disable “missing docstring” warnings at a file-level in Pylint.

### Using Pylint directly
One way to disable the missing docstring warnings is to use the `--disable` option when running Pylint directly from the command line. The `--disable` option is followed by a list of individual warning codes to disable. The code for the missing docstring warning is `C0111`.

Here’s an example command to run Pylint and disable the missing docstring warnings for a specific file:

```
$ pylint --disable=C0111 myfile.py
```

This command will run Pylint on `myfile.py` and disable the `C0111` warning, which is specifically for missing docstrings.

### Using a configuration file
Another way to disable the missing docstring warnings is to use a configuration file. Pylint reads configuration files to obtain a set of options and settings for how it should be run. 

To disable the missing docstring warnings using a configuration file, create a `.pylintrc` file in the root directory of your project (if you don't already have one) and add the following lines:

```
[MESSAGES CONTROL]
disable=C0111
```

This will disable the `C0111` warning for all files in the project. If you want to disable the warning for only one file, use the following format:

```
[MASTER]
disable=C0111

[TYPECHECK]
files-output=no

[MESSAGES CONTROL]
disable=C0111

[REPORTS]
output-format=text
```

Add the file path after the `files-output` option in the `TYPECHECK` section. 

### Disabling warnings in code
The final way to disable missing docstring warnings is to disable the warnings directly in code using comments. This is useful if you only want to disable the warning for a specific part of the file.

To disable the warning for a single line, add the following comment before the line:

```
# pylint: disable=C0111
```

To disable the warning for a block of code, add the following comments before and after the code:

```
# pylint: disable=C0111
...
# pylint: enable=C0111
```

### Conclusion
Python developers often use Pylint to ensure their code is of high quality. One of Pylint's default rules is checking if there are any missing docstrings in the code. If you have an excellent reason to skirt around this rule, you can disable the warnings in three approaches - the `--disable` method, using a configuration file, or disabling the warning in your code with comments.
