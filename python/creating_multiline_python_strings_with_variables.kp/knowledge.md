---
title: What is the process for producing a multiline Python string that contains variables within the text?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use f-strings to create a multiline Python string with inline variables.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, sometimes we need to create a string that spans multiple lines. This is typically done using triple quotes, like so:

```
my_string = """This is a
multiline
string."""
```

However, what if we need to include variables within this multiline string? This is where things can get a bit trickier. In this guide, we'll explore several ways to create a multiline Python string with inline variables.

Section 2: Using f-strings
One approach to creating a multiline Python string with inline variables is to use f-strings. F-strings are a feature introduced in Python 3.6 that allow for inline variable interpolation in strings.

Here's an example:

```
name = "Alice"
age = 30
my_string = f"""My name is {name} and I am {age} years old.
This is a
multiline
string."""
```

In this case, we're using f-strings to include the values of "name" and "age" within the string. Note that we're using triple quotes to create the multiline string.

Section 3: Using string concatenation
Another approach to creating a multiline Python string with inline variables is to use string concatenation. This involves breaking up the string into multiple smaller strings and concatenating them together with the variable values.

Here's an example:

```
name = "Bob"
age = 40
my_string = "My name is " + name + " and I am " + str(age) + " years old.\n" \
            "This is a\n" \
            "multiline\n" \
            "string."
```

In this case, we're using the "+" operator to concatenate multiple strings together, and we're also using the "\n" character to create new lines in the string. Note that we need to convert "age" to a string using the "str()" function before we can concatenate it.

Section 4: Using the join method
A third approach to creating a multiline Python string with inline variables is to use the "join" method. This involves creating a list of smaller strings and then joining them together with the variable values.

Here's an example:

```
name = "Charlie"
age = 50
my_list = ["My name is ", name, " and I am ", str(age), " years old.\n",
           "This is a\n",
           "multiline\n",
           "string."]
my_string = "".join(my_list)
```

In this case, we're creating a list of strings that we want to join together, and we're using the "".join() method to join them together with empty strings. This creates a multiline string that includes the variable values.

Section 5: Conclusion
There are several ways to create a multiline Python string with inline variables. You can use f-strings, string concatenation, or the join method, depending on your preference and the specific requirements of your code. By understanding these techniques, you can easily create complex strings that include variables and span multiple lines.
