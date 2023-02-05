---
title: Getting the result of subprocess.call()
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The output of subprocess.call() can be retrieved by assigning it to a variable and then printing the variable.
---

**Contents**

[TOC]

# Section 1: Overview

Subprocess.call() is a Python module that allows users to run external commands from within a Python script. It can be used to execute a single command or a list of commands, and it returns the output of the command(s) as an integer.

# Section 2: Syntax

The syntax for using subprocess.call() is as follows:

```
subprocess.call(args, *, stdin=None, stdout=None, stderr=None, shell=False, cwd=None, timeout=None)
```

Where 'args' is the command or list of commands to be executed.

# Section 3: Retrieving Output

The output of the command(s) can be retrieved by assigning the return value of the subprocess.call() to a variable. For example:

```
result = subprocess.call(args)
```

The 'result' variable will contain the output of the command(s) as an integer.

# Section 4: Example

For example, the following code will execute the 'echo' command and store the output in the 'result' variable:

```
result = subprocess.call(['echo', 'Hello World!'])
```

The 'result' variable will contain the output of the command as an integer.
