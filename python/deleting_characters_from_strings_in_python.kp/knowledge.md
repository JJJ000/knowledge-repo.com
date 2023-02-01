---
title: How to remove a character from a string using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the built-in string method `replace` to delete a character from a string in Python.
---

**Contents**

[TOC]

### Step 1: Identify the Character to be Deleted

The first step is to identify the character to be deleted from the string. This can be done by using the `index()` method to get the index of the character.

### Step 2: Create a New String

Once the index of the character to be deleted is known, a new string can be created by slicing the string up to the index of the character.

### Step 3: Concatenate the Strings

The new string can then be concatenated with the part of the original string after the character to be deleted.

### Step 4: Assign the New String to the Original String

Finally, the new string can be assigned to the original string, thus replacing the original string with the new string without the deleted character.
