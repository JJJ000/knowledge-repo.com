---
title: Rename a key in a dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can change the name of a key in a dictionary in Python by assigning the new key name to the value of the old key.
---

**Contents**

[TOC]

### 1. Accessing the Dictionary

In order to change the name of a key in a dictionary, we must first access the dictionary. This can be done using the syntax `dictionary_name[key_name]`.

### 2. Changing the Key Name

Once we have accessed the dictionary, we can change the name of the key by using the syntax `dictionary_name[new_key_name] = dictionary_name[old_key_name]`. This will create a new key with the desired name and assign the value of the old key to it.

### 3. Deleting the Old Key

Once the new key has been created, the old key can be deleted using the syntax `del dictionary_name[old_key_name]`. This will remove the old key and its associated value from the dictionary.

### 4. Updating the Dictionary

Finally, the updated dictionary can be saved by using the syntax `dictionary_name.update()`. This will update the dictionary with the new key name and value, and remove the old key.
