---
title: Supplying a dictionary to a function as keyword arguments
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Passing a dictionary to a function as keyword parameters in Python is done by using the double asterisk (**) operator before the dictionary.
---

**Contents**

[TOC]

#### Syntax

The syntax for passing a dictionary to a function as keyword parameters is:

```
function_name(**dictionary_name)
```

#### Example

For example, if we have a function called `print_info()` and a dictionary called `person_info` with the keys `name`, `age` and `city`, we can call the function and pass the dictionary as keyword parameters like this:

```
print_info(**person_info)
```

#### Output

This will print out the values of the dictionary `person_info` in the function `print_info()`. For example, if the values of the dictionary are `John`, `25` and `New York`, the output will be:

```
Name: John
Age: 25
City: New York
```

#### Benefits

Passing a dictionary to a function as keyword parameters is a convenient way to pass a large number of arguments to a function without having to explicitly specify each argument. It also makes the code more readable and easier to maintain.
