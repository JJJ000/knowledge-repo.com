---
title: What is the purpose of including #!/usr/bin/env Python on the first line of a Python script?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: This is a shebang line which tells the operating system which interpreter to use when running the script.
---

**Contents**

[TOC]

# Overview

The `#!` (also known as a shebang) is a special marker that is used to indicate the interpreter that should be used to execute a script. By writing `#!/usr/bin/env python` on the first line of a Python script, the script can be executed directly without having to explicitly call the Python interpreter.

# Why Use `#!/usr/bin/env python`?

Using `#!/usr/bin/env python` allows the script to be executed regardless of the location of the Python interpreter. This is because `/usr/bin/env` is a special directory that contains a list of all available interpreters. By using `env`, the script will automatically use the correct interpreter, regardless of where it is located on the system.

# Advantages

Using `#!/usr/bin/env python` has several advantages over explicitly calling the Python interpreter. For example:

- It allows the script to be executed on any system, regardless of where the Python interpreter is located.
- It allows the script to be executed without having to explicitly call the Python interpreter.
- It allows the script to use the correct version of the Python interpreter, even if multiple versions are installed on the system.
