---
title: Eliminating specific characters from a given string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `str.replace()` method to remove a list of characters from a string in Python.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, it is possible to remove a list of characters from a string using different methods. In this article, we will explore some of the common methods to remove a list of characters from a string in Python.

Section 2: Using the translate() method
The translate() method is a built-in method in Python that can be used to remove a list of characters from a string. Here is an example:

```
string = "Hello, World!"
remove_chars = "l, o"
translation_table = str.maketrans("", "", remove_chars)
new_string = string.translate(translation_table)

print(new_string)
```

In the example above, we first define the string we want to remove characters from. We also define the list of characters we want to remove. We then create a translation table using the maketrans() method, which takes three arguments: the first argument is an empty string, the second argument is the list of characters we want to remove, and the third argument is another empty string. We then apply the translate() method on the original string, passing in the translation table we created. Finally, we print the new string without the removed characters.

Section 3: Using the replace() method
The replace() method is another built-in method in Python that can be used to remove a list of characters from a string. Here is an example:

```
string = "Hello, World!"
remove_chars = ["l", "o"]
for char in remove_chars:
    string = string.replace(char, "")

print(string)
```

In the example above, we define the string we want to remove characters from, and we define the list of characters we want to remove. We then loop through each character in the list and use the replace() method to replace it with an empty string. Finally, we print the new string without the removed characters.

Section 4: Using a list comprehension
Another way to remove a list of characters from a string in Python is to use a list comprehension. Here is an example:

```
string = "Hello, World!"
remove_chars = ["l", "o"]
new_string = "".join([char for char in string if char not in remove_chars])

print(new_string)
```

In the example above, we define the string we want to remove characters from, and we define the list of characters we want to remove. We then use a list comprehension to create a new list of characters that exclude the ones we want to remove. We then join the new list of characters together to form a new string. Finally, we print the new string without the removed characters.
