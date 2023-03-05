---
title: What is the procedure for substituting whitespaces with an underscore?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the string method `.replace()` to replace whitespace ` ` with underscore `\_`. 

Example 

```
my\_string = `Hello there world`
new\_string = my\_string.replace(` `, `\_`)
print(new\_string)
```

Output

```
Hello\_there\_world
```
---

**Contents**

[TOC]

## Introduction
In Python, whitespaces are characters like space, tab, newline, etc. Sometimes, we need to replace these whitespaces with other characters like underscore (_). In this tutorial, we will learn how to replace whitespaces with underscores in Python.

## Using replace() function
The easiest way to replace whitespaces with underscores is to use the replace() function. We can pass the whitespace character as the first argument and underscore character as the second argument to this function. Here is an example:

```python
# Replace spaces with underscores
s = "Hello World"
s = s.replace(" ", "_")
print(s) # Output: Hello_World
```

## Using regular expressions
Another way to replace whitespaces with underscores is to use regular expressions. We can use the sub() function from the re module to replace all occurrences of whitespace characters with underscores. Here is an example:

```python
import re

# Replace spaces with underscores using regular expressions
s = "Hello    World\n\n"
s = re.sub(r'\s+', '_', s)
print(s) # Output: Hello_World_
```

In the above example, we used the regular expression '\s+' to match one or more whitespace characters. We passed this regex as the first argument to the sub() function and underscore as the second argument.

## Using translate() function
We can also use the translate() function to replace whitespaces with underscores. The translate() function takes a translation table as an argument, which specifies the replacement characters for each character in the input string. Here is an example:

```python
# Replace spaces with underscores using translate() function
s = "Hello World"
table = str.maketrans(" ", "_")
s = s.translate(table)
print(s) # Output: Hello_World
```

In the above example, we used the maketrans() function to create a translation table that maps space character to underscore character. We then passed this table to the translate() function to replace all space characters with underscores.

## Conclusion
In this tutorial, we learned how to replace whitespaces with underscores in Python. We used the replace() function, regular expressions, and translate() function to achieve this.
