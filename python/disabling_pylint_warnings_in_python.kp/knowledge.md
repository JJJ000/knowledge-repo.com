---
title: What is the procedure for turning off a pylint alert?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can disable a Pylint warning in Python by adding a comment to the code with the string `# pylint disable=<warning-name>`.
---

**Contents**

[TOC]

# Solution

## Using .pylintrc

The most common way to disable a Pylint warning is to add a configuration file, named `.pylintrc`, to your project directory. This configuration file can be used to specify which warnings and errors you want to disable for your project. To disable a specific warning, you need to add the following line to your `.pylintrc` file:

```
disable=<warning_name>
```

Where `<warning_name>` is the name of the warning you want to disable.

## Using Command Line Arguments

You can also disable a Pylint warning using command line arguments. To do this, you need to pass the `--disable` argument to the `pylint` command, followed by the name of the warning you want to disable:

```
pylint --disable=<warning_name>
```

## Using Comments

You can also disable a Pylint warning by adding a comment to the code. To do this, you need to add the following comment at the top of the file:

```
# pylint: disable=<warning_name>
```

Where `<warning_name>` is the name of the warning you want to disable.

## Using Configuration File

You can also disable a Pylint warning by adding a configuration file, named `pylint.cfg`, to your project directory. This configuration file can be used to specify which warnings and errors you want to disable for your project. To disable a specific warning, you need to add the following line to your `pylint.cfg` file:

```
disable=<warning_name>
```

Where `<warning_name>` is the name of the warning you want to disable.
