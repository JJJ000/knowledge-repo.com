---
title: The act of bringing a class from a different file into your code
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To import a class from another file in Python, use the syntax `from filename import classname`.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, we may have to split the code into multiple files for better readability, reducing redundancy, and code maintenance. To use a class or function defined in a file within another file, we have to import it.  In this article, we will look at how to import a class defined in another file in Python.

Section 2: Defining a class in a separate file
To define a class in a separate file, we write the class as usual in a file with a .py extension. For example, suppose we have a file named hello.py that contains the following code:

```
class Hello:
    def __init__(self):
        self.message = "Hello, World!"

    def display(self):
        print(self.message)
```

Section 3: Importing the class
After defining the class in the separate file, we can import it into another file. To import the class in the new file, we need to use the 'from' and 'import' keywords. For instance, to import the Hello class defined in the hello.py file, we write the following code in a new Python file:

```
from hello import Hello

hello_obj = Hello()
hello_obj.display()
```

The above code imports the Hello class defined in the hello.py file, creates an instance of the class, and calls the display method to print the message "Hello, World!".

Section 4: Conclusion
To import a class from another file in Python, we need to use the 'from' and 'import' keywords. This allows us to access and use the class and its methods defined in another file. By defining classes in separate files and importing them in other files, we can write structured and organized code that is easy to read and maintain.
