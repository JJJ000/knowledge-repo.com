---
title: What is the way to mute py.test's internal deprecation warnings?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Pass the command line argument `-p nowarnings` when running `py.test`.
---

**Contents**

[TOC]

## Introduction
Pytest is a popular testing framework in Python. Though it is very powerful, it may show some deprecated warning messages during runtime. These warnings might overshadow other important messages and errors, making it difficult to keep track of things.
In this tutorial, we will discuss how to suppress py.test internal deprecation warnings in Python.

## The  warning system in pytest

Pytest has an in-built warning system that flags you whenever a deprecated feature is detected.
Deprecation warnings are warnings indicating that the feature in question will be removed or changed in a future version of pytest. These warnings are typically intended to provide backward compatibility so that the new version isn’t purely incompatible with previous versions.

However, these warnings can be disruptive and distracting, particularly when dealing with third-party modules.
In the next section, we’ll discuss how to suppress these warnings.

## Suppressing deprecation warnings in pytest
Pytest provides a command-line option “`-p no:warnings`” to disable warning messages altogether.

Here’s an example usage:

```
py.test --disable-warnings  # disable all warning outputs
```

Not all warning messages might be irrelevant to your development tasks. Hence ignoring all of them might not be appropriate.
Another option is to allow warnings but suppress the specific deprecation warnings you wish to suppress.

To suppress warnings, you must set the `PYTHONWARNINGS` environment variable.

The value should be set to "ignore::pytest.RemovedInPytest4Warning" to ignore warnings from pytest version 4.x.

Here’s an example: 

```
export PYTHONWARNINGS="ignore::pytest.RemovedInPytest4Warning"
```
This will suppress all warnings that match the regex.
Note that you need to replace `4` in the above regex with the actual version of pytest that you are running.

## Conclusion
In conclusion, to suppress py.test internal deprecation warnings in Python, we can disable warnings altogether or use the `PYTHONWARNINGS` environment variable to suppress the specific deprecation warnings we want to ignore.
