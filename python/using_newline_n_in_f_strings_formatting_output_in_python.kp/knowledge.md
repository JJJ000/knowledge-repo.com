---
title: In what way can I format the output using the newline character '\n' within an f-string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the newline character `\n` within an f-string by enclosing it in curly braces preceded by the character `f`.
---

**Contents**

[TOC]

Section 1: Introduction

Python provides numerous formatting options to create strings with specific formats in the desired fashion. One of them is f-strings, which is a way to specify string literals that have embedded expressions inside them. These strings are prefixed with an 'f.' However, sometimes, you might want to include newline characters within your f-string, and this can seem a bit tricky if you're new to this.

This article aims to provide you with detailed information on how to use newline '\n' in an f-string to format output in Python.

Section 2: Using newline characters in f-strings

Using newline characters in f-strings is pretty easy. You can use the '\n' character to add a new line in your f-string. Consider the following example.

```
name = "John"
age = 25
profession = "Engineer"
f_string = f"Name: {name}\nAge: {age}\nProfession: {profession}"
print(f_string)
```
Here, we have used the '\n' character to add a new line after each piece of information. The output of this code will be:

```
Name: John
Age: 25
Profession: Engineer
```

So, as you can see, using the '\n' character in f-strings is very easy.

Section 3: Using triple quotes in f-strings

Another way to add newline characters in f-strings is by using triple quotes. Triple quotes are used to define multiline strings in Python, and they can be used in f-strings to add newlines as well.

Here's an example:

```
name = "John"
age = 25
profession = "Engineer"
f_string = f"""
Name: {name}
Age: {age}
Profession: {profession}"""
print(f_string)
```

In this example, we have used triple quotes to define a multiline string with a newline character after each piece of information. The output of this code will be the same as the previous example.

Section 4: Conclusion

So, these are the two ways to use newline '\n' in an f-string to format output in Python. You can use either the '\n' character or triple quotes to add newlines in your f-strings. However, using the '\n' character is more common and preferred as it looks cleaner and easier to read.
