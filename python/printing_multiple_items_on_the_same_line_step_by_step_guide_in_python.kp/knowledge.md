---
title: Is it possible to print multiple items consecutively on a single line?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: You can use the `end` parameter in the print function to append a space instead of a newline, allowing you to print multiple things on the same line.
---

**Contents**

[TOC]

1. Using the print() function with end parameter

You can use the end parameter in the print() function to specify what character or string should be printed at the end of each print statement. By default, the end parameter is set to '\n' which means that a newline character is added at the end of each print statement, creating a new line. Here's how you can use the end parameter to print multiple things on the same line:

```
print("Hello", end='')
print("world", end='')
print("!")
```

Output: `Hello world!`

2. Using the separator parameter

The print() function also has a separator parameter that specifies what character or string should be used to separate the different arguments passed to it. By default, the separator is set to ' ' (space character). Here's how you can use the separator parameter to print multiple things on the same line:

```
print("Hello", "world", "!", sep='')
```

Output: `Helloworld!`

3. Using string concatenation

You can concatenate multiple strings together to print them on the same line. Here's an example:

```
name = "John"
age = 28
print("My name is " + name + " and I am " + str(age) + " years old")
```

Output: `My name is John and I am 28 years old`

4. Using formatted strings

You can also use formatted strings to print multiple things on the same line. Here's an example:

```
name = "John"
age = 28
print(f"My name is {name} and I am {age} years old")
```

Output: `My name is John and I am 28 years old`

Formatted strings make it easier to combine variables and strings together in a single line of code.
