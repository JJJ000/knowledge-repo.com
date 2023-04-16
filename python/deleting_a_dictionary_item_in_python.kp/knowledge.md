---
title: Remove an entry from the dictionary if the key is present
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: If the key exists, you can delete the dictionary item by using the del keyword.
---

**Contents**

[TOC]

# Section 1: Finding the Key

In order to delete a dictionary item in Python, the first step is to find the key. This can be done by using the `in` operator.

# Section 2: Deleting the Item

Once the key has been found, the item can be deleted using the `del` keyword.

# Section 3: Syntax

The syntax for deleting a dictionary item is as follows:

`del dictionary[key]`

# Section 4: Example

For example, if we have a dictionary called `my_dict` with the key `'foo'`, we can delete the item associated with that key by using the following code:

`del my_dict['foo']`
