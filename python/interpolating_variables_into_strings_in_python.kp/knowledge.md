---
title: What is the syntax for inserting a variable's value into a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the format() method or f-strings to interpolate variables into strings in Python.
---

**Contents**

[TOC]

**Using the f-string Method**

The f-string method is the most common and preferred way to interpolate variables into strings in Python. An f-string is a string literal that is prefixed with the letter 'f' and can contain any type of expression that can be evaluated, including variables. To interpolate a variable into a string using the f-string method, the variable must be placed inside curly brackets within the string. The following example shows how to interpolate a variable into a string using the f-string method:

```
name = "John"
print(f"Hello, {name}!")
```

The output of the above code will be:

```
Hello, John!
```

**Using the format() Method**

The format() method is another way to interpolate variables into strings in Python. To use the format() method, the variable must be placed inside curly brackets within the string. The following example shows how to interpolate a variable into a string using the format() method:

```
name = "John"
print("Hello, {}!".format(name))
```

The output of the above code will be:

```
Hello, John!
```

**Using the % Operator**

The % operator is an older method of interpolating variables into strings in Python. To use the % operator, the variable must be placed after the % symbol within the string. The following example shows how to interpolate a variable into a string using the % operator:

```
name = "John"
print("Hello, %s!" % name)
```

The output of the above code will be:

```
Hello, John!
```

**Using the format_map() Method**

The format_map() method is another way to interpolate variables into strings in Python. To use the format_map() method, the variable must be placed inside curly brackets within the string. The following example shows how to interpolate a variable into a string using the format_map() method:

```
name = "John"
print("Hello, {name}!".format_map(vars()))
```

The output of the above code will be:

```
Hello, John!
```
