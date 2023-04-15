---
title: Executing a bash script from inside a Python program
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To run a bash script from within Python, use the subprocess module to call the script as a subprocess/command-line executable.
---

**Contents**

[TOC]

Using the `subprocess` module

The `subprocess` module is a built-in module that allows you to spawn new processes, connect to their input/output/error pipes, and obtain their return codes. You can use this module to execute a bash command or script from within Python.

Here's an example of how to use the `subprocess` module to run a bash script named `myscript.sh`:

```
import subprocess

subprocess.call(["bash", "myscript.sh"])
```

In this example, we're calling the `subprocess.call()` function with a list of arguments. The first argument is the name of the shell executable (`bash`), and the second argument is the name of the script we want to run (`myscript.sh`).

Using the `os` module

The `os` module provides functions for interacting with the operating system. You can use the `os.system()` function to run a bash command or script from within Python.

Here's an example of how to use the `os` module to run a bash script named `myscript.sh`:

```
import os

os.system("bash myscript.sh")
```

In this example, we're calling the `os.system()` function with a single argument, which is the command we want to execute (`bash myscript.sh`).

Using the `subprocess.run()` function

The `subprocess` module also provides a `run()` function that allows you to execute a command and capture its output. You can use this function to run a bash script from within Python and capture its output.

Here's an example of how to use the `subprocess.run()` function to run a bash script named `myscript.sh`:

```
import subprocess

result = subprocess.run(["bash", "myscript.sh"], capture_output=True)
print(result.stdout)
```

In this example, we're calling the `subprocess.run()` function with a list of arguments, just like we did with `subprocess.call()`. The `capture_output=True` argument causes the function to capture the output of the command and store it in the `stdout` attribute of the `CompletedProcess` object that the function returns. We're then printing the captured output.

Using the `os.popen()` function

The `os.popen()` function allows you to open a pipe to an operating system command and read its output as a file-like object. You can use this function to run a bash script from within Python and read its output line by line.

Here's an example of how to use the `os.popen()` function to run a bash script named `myscript.sh`:

```
import os

output = os.popen("bash myscript.sh").readlines()
for line in output:
    print(line.rstrip())
```

In this example, we're calling the `os.popen()` function with a single argument, just like we did with `os.system()`. The `readlines()` method reads the output of the command as a list of lines. We're then iterating over the lines and printing them, stripped of their trailing newlines.
