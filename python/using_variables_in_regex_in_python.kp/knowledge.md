---
title: What is the syntax for inserting a variable into a regular expression?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the re.escape() function to escape the variable before using it in the regular expression.
---

**Contents**

[TOC]

#Section 1 - Creating the Regular Expression

To use a variable inside a regular expression in Python, you first need to create the regular expression. Regular expressions are strings of characters that are used to match patterns in other strings. In Python, you can create a regular expression using the re module. To do this, you use the re.compile() method and pass in the regular expression as a string.

#Section 2 - Adding the Variable

Once you have created the regular expression, you can add the variable by using the re.sub() method. This method takes two arguments: the regular expression and the replacement string. The replacement string can be a variable, which will be used to match the pattern in the regular expression.

#Section 3 - Using the re.sub() Method

Once you have added the variable to the regular expression, you can use the re.sub() method to search for and replace the pattern with the variable. This method takes three arguments: the regular expression, the replacement string, and the string to search. The re.sub() method will search the string for the pattern in the regular expression and replace it with the replacement string.

#Section 4 - Example

For example, let's say we have a string that contains a number and we want to replace it with a variable. We could use the following code to do this:

import re

my_string = "This is a string with a number: 123"

my_variable = "456"

regex = re.compile("\d+")

new_string = re.sub(regex, my_variable, my_string)

print(new_string)

This would print out: "This is a string with a number: 456"
