---
title: Obtaining live results through subprocess
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `subprocess.PIPE` argument and the `communicate()` method to get real-time output from a subprocess in Python.
---

**Contents**

[TOC]

Section 1: Background
In Python, subprocess module is used to spawn new processes and connect to their input/output/error pipes. It provides more powerful facilities compared to the os module. One of these facilities is getting real-time output from a subprocess.

Section 2: Using subprocess.Popen
To get real-time output, we can use the Popen constructor provided by subprocess module. This constructor returns a Popen object that represents the new process spawned. We can read the standard output of the subprocess from the stdout attribute of the Popen object.

Here's an example:

```python
import subprocess

# start the subprocess
process = subprocess.Popen(['ping', '8.8.8.8'], stdout=subprocess.PIPE)

# read output line by line as it comes
for line in process.stdout:
    print(line.decode())
```

This example starts the 'ping' command with the IP address '8.8.8.8' as an argument. It then reads the output of the process line by line from the stdout attribute of the Popen object and prints it to the console using the 'print' function.

Section 3: Using subprocess.run
Another way to get real-time output is to use the run() function of the subprocess module. This function runs a command and returns a CompletedProcess object that contains the output of the command.

Here's an example:

```python
import subprocess

# start the subprocess
process = subprocess.run(['ping', '8.8.8.8'], stdout=subprocess.PIPE, text=True, check=True)

# print the output
print(process.stdout)
```

This example starts the 'ping' command with the IP address '8.8.8.8' as an argument. It then runs the command and returns a CompletedProcess object. The CompletedProcess object contains the output of the command, which we can access using the 'stdout' attribute.

Section 4: Conclusion
Both subprocess.Popen and subprocess.run can be used to get real-time output from a subprocess in Python. The choice between the two depends on the requirements of the application. If we need to read the output line by line, we can use subprocess.Popen. If we need to get the output in one go, we can use subprocess.run.
