---
title: What is the way to execute an external command in Python in an asynchronous manner?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `subprocess` module`s `Popen` function to start the external command in a separate process and use the `communicate` function to interact with the process while allowing the parent program to continue running.
---

**Contents**

[TOC]

### Using the `subprocess` module

The `subprocess` module in Python can be used to run external commands asynchronously. 

Here's an example code snippet that demonstrates how to run a command asynchronously using `subprocess`.

```python
import subprocess

# Define command to execute
command = ['ping', '8.8.8.8', '-c', '5']

# Execute command asynchronously using subprocess
process = subprocess.Popen(command, stdout=subprocess.PIPE, stderr=subprocess.PIPE)

# Wait for the process to complete
stdout, stderr = process.communicate()

# Print stdout and stderr output
print("Stdout:", stdout.decode())
print("Stderr:", stderr.decode())
```
In the code snippet above, we define the command we want to execute as a list of arguments. We then use `subprocess.Popen` to create a new process to execute the command asynchronously. We pass `stdout=subprocess.PIPE` and `stderr=subprocess.PIPE` to capture the process's standard output and error output, respectively. Finally, we call `communicate()` on the process object to wait for the command to complete and retrieve its output.

### Using the `asyncio` module

Another way to run an external command asynchronously in Python is to use the `asyncio` module. `asyncio` allows us to write asynchronous code in a more idiomatic way using coroutines and event loops.

Here's an example code snippet that demonstrates how to run a command asynchronously using `asyncio`.

```python
import asyncio
import subprocess

async def run_command(command):
    process = await asyncio.create_subprocess_exec(*command, stdout=subprocess.PIPE, stderr=subprocess.PIPE)
    stdout, stderr = await process.communicate()
    return (stdout, stderr)

async def main():
    command = ['ping', '8.8.8.8', '-c', '5']
    stdout, stderr = await run_command(command)
    print("Stdout:", stdout.decode())
    print("Stderr:", stderr.decode())

asyncio.run(main())
```

In the code above, we define a coroutine `run_command` that takes a command as input and returns the command's standard output and error output. We use `asyncio.create_subprocess_exec` to create a new process to execute the command asynchronously. We then await the process's completion and retrieval of its output.

We also define a `main` coroutine to execute our `run_command` coroutine and print the command's output.

Finally, we call `asyncio.run` on the `main` coroutine to run the entire async program.

### Using the `concurrent.futures` module

The `concurrent.futures` module provides a way to execute code asynchronously using the `ThreadPoolExecutor` and `ProcessPoolExecutor` classes. 

Here's an example code snippet that demonstrates how to run a command asynchronously using `concurrent.futures`.

```python
import concurrent.futures
import subprocess

def run_command(command):
    process = subprocess.Popen(command, stdout=subprocess.PIPE, stderr=subprocess.PIPE)
    stdout, stderr = process.communicate()
    return (stdout, stderr)

with concurrent.futures.ThreadPoolExecutor() as executor:
    command = ['ping', '8.8.8.8', '-c', '5']
    future = executor.submit(run_command, command)
    stdout, stderr = future.result()
    print("Stdout:", stdout.decode())
    print("Stderr:", stderr.decode())
```

In the code above, we define a function `run_command` that takes a command as input and returns the command's standard output and error output. We use the `subprocess.Popen` method to create a new process to execute the command asynchronously.

We then use a `ThreadPoolExecutor` to execute the `run_command` function in a separate thread. Finally, we retrieve the command's output using the `future.result()` method.

### Using the `threading` module

The `threading` module can also be used to run a command asynchronously in a separate thread.

Here's an example code snippet that demonstrates how to run a command asynchronously using `threading`.

```python
import threading
import subprocess

def run_command(command):
    process = subprocess.Popen(command, stdout=subprocess.PIPE, stderr=subprocess.PIPE)
    stdout, stderr = process.communicate()
    print("Stdout:", stdout.decode())
    print("Stderr:", stderr.decode())

command = ['ping', '8.8.8.8', '-c', '5']
thread = threading.Thread(target=run_command, args=(command,))
thread.start()
```

In the code above, we define a `run_command` function that takes a command as input and prints the command's standard output and error output. We use `subprocess.Popen` to create a new process to execute the command asynchronously.

We then create a new `Thread` object and pass the `run_command` function as its target. We start the thread using the `thread.start()` method.

Note that in the above solution, we don't wait for the command to complete before exiting the program. If you need to wait for the command to complete before continuing execution, you can call the `thread.join()` method after starting the thread.
