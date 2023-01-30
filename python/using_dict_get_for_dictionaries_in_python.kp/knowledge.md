---
title: What are the advantages of using dict.get(key) over dict[key]?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: dict.get(key) returns None instead of raising an error when the key is not found, whereas dict[key] will raise a KeyError.
---

**Contents**

[TOC]

# Advantages of using dict.get()

dict.get() provides a way to access a value in a dictionary without raising a KeyError if the key does not exist. This allows the programmer to specify a default value to be returned instead of raising an exception if the key does not exist.

# Syntax

The syntax for dict.get() is as follows:

dict.get(key[, default])

The key argument is the key of the element to be returned from the dictionary. The default argument is an optional argument that specifies the value to be returned if the key does not exist in the dictionary.

# Example

For example, if you have a dictionary like this:

my_dict = {'name': 'John', 'age': 27}

You can access the value for the 'name' key using the dict.get() method like this:

name = my_dict.get('name')

This will return the value 'John', since the 'name' key exists in the dictionary.

If you try to access a key that does not exist in the dictionary, you will get None as the return value:

not_in_dict = my_dict.get('not_in_dict')

This will return None since the 'not_in_dict' key does not exist in the dictionary.

# Advantages Over dict[key]

dict.get() is more convenient than using the dict[key] syntax, since it allows the programmer to specify a default value to be returned if the key does not exist. This can save the programmer from having to write extra code to handle a KeyError exception.
