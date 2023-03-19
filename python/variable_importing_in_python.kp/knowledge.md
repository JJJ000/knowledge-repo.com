---
title: Is there a way to bring in variables from a different file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To import variables from another file in Python, you can use the `import` statement followed by the name of the file (without the `.py` extension) and then access the variables using dot notation.
---

**Contents**

[TOC]

Section 1: Introduction
There are times when you may find yourself wanting to use variables defined in another Python file in your current script. Rather than defining those variables again in your current file, you can import them from the other file. This can save you a lot of time, and make your code more modular and easier to manage. In this answer, we will discuss how to import variables from another file in Python.

Section 2: Defining Variables to Import
Before you can import variables from another file, you need to define those variables in the other file. Let's say you have a file called "variables.py", and in that file, you have defined the following variables:

```
name = "John Doe"
age = 30
height = 180.5
```
These variables can be of any type, including strings, integers, floats, lists, tuples, and dictionaries.

Section 3: Importing Variables
To import variables from a file, you can use the "import" statement. Here is an example of how you can import the variables defined in "variables.py" into your current script:

```
import variables

print(variables.name)
print(variables.age)
print(variables.height)
```
In this example, we are importing the entire "variables.py" file and using the variable names defined in that file. We can access these variables using the "variables." prefix. When we run this script, we will see the following output:

```
John Doe
30
180.5
```

Section 4: Importing Specific Variables
If you only want to import specific variables from a file, you can use the "from" statement. Here is an example:

```
from variables import name, age

print(name)
print(age)
```

In this example, we are importing only the "name" and "age" variables from "variables.py". We are not importing the "height" variable. When we run this script, we will see the following output:

```
John Doe
30
```

Using this method, we don't need to use the "variables." prefix, since we are importing only the specific variables we need.

Conclusion:
Importing variables from another file in Python is straightforward. You can use the "import" statement to import the entire file, or the "from" statement to import specific variables. This can make your code more modular, easier to manage, and save you time when you need to reference variables in another file.
