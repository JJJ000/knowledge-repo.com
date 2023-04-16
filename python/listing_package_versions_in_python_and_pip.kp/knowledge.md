---
title: What are all the versions of a package that can be accessed using Python and pip?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To list all versions of a package that`s available, use the command `pip list --outdated --format=columns` in the Python terminal.
---

**Contents**

[TOC]

## Using pip

Using the pip command line tool, you can list all versions of a package that is available by running the following command:

`pip list --outdated`

This will list all versions of the package that are currently installed and available.

## Using Python

You can also list all versions of a package that is available using Python. To do this, you can use the pkg_resources module.

For example, to list all versions of a package named 'my_package', you can run the following command:

`import pkg_resources`

`for dist in pkg_resources.working_set:`

`    if dist.project_name == 'my_package':`

`        print(dist.version)`

This will list all versions of the package that are currently installed and available.
