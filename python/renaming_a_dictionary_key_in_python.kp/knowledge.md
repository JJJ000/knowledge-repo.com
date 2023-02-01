---
title: Change the name of a dictionary key
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can rename a dictionary key in Python by assigning the new key name to the value of the old key.
---

**Contents**

[TOC]

#1 Renaming a Dictionary Key
Renaming a dictionary key in Python is a simple process. The syntax is as follows:

dict_name[new_key] = dict_name.pop(old_key)

#2 Example
For example, if we have a dictionary called ‘my_dict’ with a key called ‘old_key’ that we want to rename to ‘new_key’, we can do the following:

my_dict[new_key] = my_dict.pop(old_key)

#3 Verification
To verify that the key has been renamed, we can print out the dictionary:

print(my_dict)

#4 Output
The output should show that the key has been renamed:

{'new_key': 'value'}
