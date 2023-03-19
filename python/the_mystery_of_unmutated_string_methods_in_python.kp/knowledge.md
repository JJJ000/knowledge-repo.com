---
title: Why do string methods like .replace or .strip not cause a mutation or modification to the string they are called on?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-15 00:00:00
updated_at: 2023-03-15 00:00:00
tldr: Strings are immutable objects in Python, meaning their values cannot be changed after they are created, so calling a string method returns a new string with the desired changes rather than modifying the original string.
---

**Contents**

[TOC]

Introduction
Python is an object-oriented programming language that works with objects, including strings. One of the distinguishing features of objects in Python is that they can be mutable or immutable. Mutable objects allow modifying and updating their content, whereas immutable objects are unchangeable.

One of the most common operations with strings is to manipulate their content using built-in string methods. These methods allow performing various string transformations, such as replacing substrings or removing whitespace. However, when using these methods in Python, changes to the original string do not occur. This behavior can be confusing for beginners, and this article explores the reasons behind it.

Section 1: Strings are immutable
In Python, strings are immutable objects, meaning their content cannot be modified after creation. When a string is created, a new object is allocated in memory, and its value remains unchanged throughout its lifetime. Any operation that modifies the string's content creates a new string object instead of changing the existing one.

For example, consider the following code snippet:

```
text = "Hello, World!"
text.replace("Hello", "Hola")
print(text)
```

The call to the `replace` method creates a new string object with the modified content, but the original `text` object remains unchanged. Therefore, the output of this code is still `"Hello, World!"`.

Section 2: String methods return new objects
When a string method is called, it returns a new string object with the modified content. The original string remains unchanged, and any subsequent operations are performed on the returned object.

For example, consider the following code:

```
text = "   Hello, World!   "
text.strip()
print(text)
```

The `strip` method removes whitespace from both ends of the string and returns a new string object with the modified content. However, the original `text` object remains unchanged, and the output of this code is still the same: `"   Hello, World!   "`.

Section 3: Assignment creates new references
In Python, assignment statements create new references to objects instead of copying them. When a string is assigned to a new variable, both variables refer to the same object in memory. Therefore, any operations that modify the string content affect both variables.

For example, consider the following code snippet:

```
text = "Hello, World!"
new_text = text
new_text.replace("Hello", "Hola")
print(text)
```

The `new_text` variable refers to the same object as `text`, meaning that any changes made to `new_text` also affect `text`. However, the `replace` method creates a new object with the modified content, and the original object remains unchanged. Therefore, the output of this code is still `"Hello, World!"`.

Section 4: Conclusion
In conclusion, calling a string method does not modify the string in Python because strings are immutable objects, and any operation that modifies their content creates a new object instead of changing the original one. String methods return new objects with the modified content, and assignment statements create new references to objects instead of copying them. Understanding these concepts is essential when working with strings in Python and can help avoid unexpected behavior and errors.
