---
title: Shell=true in the subprocess module means that the command will be executed through the user's default shell
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Shell=True allows the subprocess to run in the same environment as the shell, enabling it to access shell commands.
---

**Contents**

[TOC]

# What is Shell?
Shell is a user interface for access to an operating system's services. It provides a command line interface for the users to interact with the operating system.

# What is Subprocess?
Subprocess is a module in Python that allows users to spawn new processes, connect to their input/output/error pipes, and obtain their return codes. This module provides a lot of control over the new processes and can be used to run system commands, as well as start and monitor background processes.

# What is Shell=True?
Shell=True is an argument in the subprocess module that specifies that the command to be executed is a shell command. This argument is necessary when the command to be executed contains shell-specific features, such as piping, redirection, variable expansion, etc. 

# What Does Shell=True Do?
Shell=True allows the subprocess module to execute the command as if it were executed in a shell. This is necessary when the command requires shell-specific features, such as piping, redirection, variable expansion, etc. Without this argument, the command will not be executed properly.
