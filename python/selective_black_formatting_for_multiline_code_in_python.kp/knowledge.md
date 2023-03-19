---
title: The task of the black formatter is to overlook particular code sections that span across multiple lines
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use triple quotes (```) to comment out the multi-line code in Python.
---

**Contents**

[TOC]

Ignoring specific multi-line code in Python

Sometimes, while working with multi-line code, we may want to ignore specific lines of code while executing the program. In Python, we have a few ways to achieve this, some of which are discussed below:

1. Using comments

One of the easiest and most popular ways to ignore specific lines of code in Python is by using comments. Comments in Python start with a hash (#) symbol, and any code written after the hash symbol is not executed by the interpreter. 

Here's an example:

```
# This line will be ignored by the interpreter
print("This line will be executed")
```

Similarly, we can comment out any code that we want to ignore, like this:

```
print("This line will be executed")
# print("This line will be ignored")
print("This line will be executed too")
```

In the above example, the second line is commented out and will be ignored by the interpreter.

2. Using a try-except block

Another way to ignore specific lines of code in Python is by using a try-except block. We can wrap the code that we want to ignore in a try block, and catch any exceptions that are raised in the except block. This way, even if an exception is raised, the program will continue to execute.

Here's an example:

```
try:
    # This code will be ignored
    x = 1/0
except:
    pass

print("This line will be executed")
```

In the above example, the code inside the try block will raise a ZeroDivisionError, but since we have caught the exception in the except block and used the pass statement to do nothing, the program will not halt and will continue to execute the rest of the code.

3. Using a function

Another way to ignore specific lines of code in Python is by putting the code that we want to ignore inside a function, and then not calling the function. This way, the code inside the function will not be executed.

Here's an example:

```
def ignore_this_code():
    # This code will be ignored
    print("This line will be ignored")
    print("This line will be ignored too")

print("This line will be executed")

# We're not calling the function here, so the code inside the function will not be executed
# ignore_this_code()
```

In the above example, we have defined a function called "ignore_this_code", and put the lines we want to ignore inside it. Since the function is not called, the code inside the function will not be executed.

4. Using a preprocessor directive

Finally, we can use a preprocessor directive to ignore specific lines of code in Python. Preprocessor directives are special statements that are processed by the Python interpreter before the code is executed. One such directive is the "#pragma" statement that is used in C and C++.

Here's an example:

```
#pragma python2
print "This line will be executed in Python 2.x only"
# This line will be ignored by the Python 3.x interpreter
#pragma python3
print("This line will be executed in Python 3.x only")
```

In the above example, we have used the "#pragma" statement to switch between Python 2.x and Python 3.x code. Any code that is not relevant to the current version of Python will be ignored by the interpreter.
