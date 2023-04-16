---
title: What does the command "pip install --user ..." do?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The `pip install --user` command allows users to install packages to their local user directory, instead of the system-wide directory.
---

**Contents**

[TOC]

# Overview

The "pip install --user ..." command is used to install Python packages into a user's home directory instead of the global directory. This allows users to install packages without administrator privileges.

# Advantages

The primary advantage of using the "pip install --user ..." command is that it allows users to install packages without administrator privileges. This is especially useful in environments where users do not have access to the global installation directory.

# Syntax

The syntax for the "pip install --user ..." command is as follows:

```
pip install --user <package_name>
```

Where <package_name> is the name of the package to install.

# Example

For example, to install the requests package, the following command can be used:

```
pip install --user requests
```
