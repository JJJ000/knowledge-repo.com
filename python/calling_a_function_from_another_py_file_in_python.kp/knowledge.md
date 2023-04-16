---
title: What is the syntax for calling a function from another .py file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can call a function from another .py file in Python by using the `import` statement.
---

**Contents**

[TOC]

# Section 1: Import the File

In order to call a function from another .py file, you must first import the file. This can be done using the `import` statement.

For example, if you wanted to import a file called `my_file.py`, you could use the following statement:

`import my_file`

# Section 2: Access the Function

Once the file is imported, you can access the function within the file by using the following syntax:

`my_file.function_name()`

Where `function_name` is the name of the function you want to call.

# Section 3: Call the Function

To actually call the function, you need to use the following syntax:

`my_file.function_name()`

This will execute the code within the function, and any return values will be returned to the calling code.

# Section 4: Example

For example, if the `my_file.py` file contains the following function:

```
def say_hello():
    print("Hello!")
```

You can call the function using the following statement:

`my_file.say_hello()`

This will print out the string `Hello!` to the console.
