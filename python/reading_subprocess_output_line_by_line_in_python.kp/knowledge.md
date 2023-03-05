---
title: Read each line of the subprocess stdout separately
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use a for loop to iterate over the lines of the stdout object returned by the subprocess module in Python.
---

**Contents**

[TOC]

## Using the `communicate()` method

The `communicate()` method is a good option if you need the output of the subprocess to be returned as a byte string. This method waits for the subprocess to finish and then returns a tuple containing the stdout and stderr outputs.

```python
import subprocess

cmd = ["ls", "-l"]
p = subprocess.Popen(
    cmd, stdout=subprocess.PIPE, stderr=subprocess.PIPE, universal_newlines=True
)
stdout, stderr = p.communicate()

for line in stdout.splitlines():
    print(line)
```

In this example, we use the `universal_newlines` argument to ensure that the output is returned as a string rather than bytes. Then, we split the stdout into lines and iterate over them using a for loop.

## Using `iter()`

Another option is to create an iterator over the stdout output of the subprocess using the `iter()` function. This allows us to iterate over the output line by line as it becomes available.

```python
import subprocess

cmd = ["ls", "-l"]
p = subprocess.Popen(
    cmd, stdout=subprocess.PIPE, universal_newlines=True
)

for line in iter(p.stdout.readline, ""):
    print(line.rstrip())
```

In this example, we use the `iter()` function to create an iterator over the `stdout` of the subprocess. We pass a callable `p.stdout.readline` as the first argument, which reads a line of `stdout` until it reaches the end of the line. The second argument of `""` tells the iterator to stop when it reaches the end of the `stdout`. Finally, we use `rstrip()` to remove any trailing whitespace from each line.

## Using a `while` loop

A third option is to use a `while` loop to read the `stdout` line by line until it has been completely processed.

```python
import subprocess

cmd = ["ls", "-l"]
p = subprocess.Popen(
    cmd, stdout=subprocess.PIPE, universal_newlines=True
)

while True:
    line = p.stdout.readline()
    if not line:
        break
    print(line.rstrip())
```

In this example, we use a `while` loop to read the `stdout` line by line until the end of the input is reached. The `readline()` method reads the next line of `stdout` and returns it as a string. We check if the line is empty and break out of the loop if it is. Finally, we use `rstrip()` to remove any trailing whitespace from each line. 

## Using a `for` loop and `split()`

A fourth option is to use a `for` loop to read the `stdout` and use the `split()` method to break the output into an array containing the lines.

```python
import subprocess

cmd = ["ls", "-l"]
p = subprocess.Popen(
    cmd, stdout=subprocess.PIPE, universal_newlines=True
)
output, error = p.communicate()

for line in output.split("\n"):
    print(line)
```

In this example, we first use the `communicate()` method to get the output of the subprocess. We then use the `split()` method to split the output into an array containing the lines. We then use a `for` loop to iterate over the array and print each line. 

Each of these options can be useful in different situations, depending on the specifics of the task you are trying to accomplish.
