---
title: Is a manifest.in required for Python projects and what content should it contain?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: A MANIFEST.in file is needed for Python projects that include non-Python files like data files, templates or static files and should list all these files to include them in the distribution package.
---

**Contents**

[TOC]

# Introduction 
In Python, a `MANIFEST.in` file is an important file that details which files should be included in the Python package or distribution. In this article, we will discuss whether Python projects need a `MANIFEST.in` file and what should be included in it.

## What is a MANIFEST.in file?
A `MANIFEST.in` file is a configuration file used in Python to specify additional files that should be included when a package or distribution is created. While the `setup.py` file is responsible for packaging and distribution of a Python project, the `MANIFEST.in` file determines which files should be included based on their file type, location, or any related instructions specified in it.

## Do Python projects need a MANIFEST.in file?
Yes, Python projects need a `MANIFEST.in` file, especially when the package or distribution contains non-Python files such as images, scripts, or data files. By default, the `setup.py` file includes only the necessary files for the package to run, such as `.py` files, without including other files that might be part of the project.

## What should be in a MANIFEST.in file?
A `MANIFEST.in` file can contain the following directives:

### Include
It is used to specify additional files or file patterns that should be included in the package or distribution. For example:

```
include README.md
include data/*.json
```
It includes the `README.md` file and all `.json` files in the `data` directory.

### Exclude
It is used to exclude files or patterns from the package or distribution. For example:

```
exclude tests/*.pyc
exclude *.log
```

It excludes all `.pyc` files in the `tests` directory and all `.log` files in the project.

### Recursive-include
It is used to include all files under a specified directory recursively. For example:

```
recursive-include templates *
```

It includes all files under the `templates` directory.

### Recursive-exclude
It is used to exclude all files under a specified directory recursively. For example:

```
recursive-exclude data *.bak
```

It excludes all `.bak` files under the `data` directory.

## Conclusion
In summary, the `MANIFEST.in` file is an essential part of packaging and distributing Python projects. It specifies which files should be included or excluded from the distribution or package, making it easier to install and use the project. Therefore, it is recommended to always include a `MANIFEST.in` file in Python projects to ensure that all necessary files are included in the distribution.
