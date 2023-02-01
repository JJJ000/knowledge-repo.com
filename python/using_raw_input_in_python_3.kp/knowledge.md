---
title: What is the syntax for using raw_input in Python 3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: In Python 3, you can use the built-in function raw\_input() to prompt the user for input and store the result as a string.
---

**Contents**

[TOC]

# Syntax
The syntax of raw_input() in Python 3 is:
```
raw_input([prompt])
```

# Parameters
The raw_input() function takes a single optional argument: prompt (Optional). It is a string that will be printed on the screen. It is used to give a hint to the user about what to input.

# Return Value
The raw_input() method reads a line from input (usually user), converts the line into a string by removing the trailing newline, and returns it.

# Example
The following example takes input from the user and prints it back.

```
# Python 3 code to demonstrate 
# working of raw_input() 

# taking input from user 
name = raw_input("Enter your name : ") 

# printing the name 
print("Name is : ", name) 
```

Output:
```
Enter your name : John
Name is : John
```
