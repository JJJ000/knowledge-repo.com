---
title: What is the procedure for executing one Python file from another?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can use the `exec` function to run another Python file from within a Python file.
---

**Contents**

[TOC]

# Using the `import` Statement

The `import` statement is the most commonly used way to run one python file from another. It allows you to import the code from one file into another file, which can then be used just like any other code.

For example, if you have a file called `foo.py` with the following code:

```python
def say_hello():
    print("Hello World!")
```

You can import this code into another file, `bar.py` with the following statement:

```python
import foo
```

Now, you can use the `say_hello()` function from `foo.py` inside `bar.py`:

```python
foo.say_hello()
```

# Using the `exec()` Function

The `exec()` function is another way to run one python file from another. It allows you to execute a string containing Python code.

For example, if you have a file called `foo.py` with the following code:

```python
def say_hello():
    print("Hello World!")
```

You can execute this code from another file, `bar.py` with the following statement:

```python
exec(open("foo.py").read())
```

Now, you can use the `say_hello()` function from `foo.py` inside `bar.py`:

```python
say_hello()
```

# Using the `subprocess` Module

The `subprocess` module is another way to run one python file from another. It allows you to run a process in a sub-process.

For example, if you have a file called `foo.py` with the following code:

```python
def say_hello():
    print("Hello World!")
```

You can execute this code from another file, `bar.py` with the following statement:

```python
import subprocess
subprocess.call(["python", "foo.py"])
```

Now, you can use the `say_hello()` function from `foo.py` inside `bar.py`:

```python
say_hello()
```

# Using the `os.system()` Function

The `os.system()` function is another way to run one python file from another. It allows you to execute a command in the operating system's shell.

For example, if you have a file called `foo.py` with the following code:

```python
def say_hello():
    print("Hello World!")
```

You can execute this code from another file, `bar.py` with the following statement:

```python
import os
os.system("python foo.py")
```

Now, you can use the `say_hello()` function from `foo.py` inside `bar.py`:

```python
say_hello()
```
