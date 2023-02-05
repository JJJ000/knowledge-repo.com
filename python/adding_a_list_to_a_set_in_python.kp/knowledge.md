---
title: Include list in set
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can add a list to a set in Python using the set.update() method.
---

**Contents**

[TOC]

1. **Creating a Set:**
   To create a set in Python, use the set() function.

2. **Adding List Items to a Set:**
   To add list items to a set, use the update() method. The update() method takes a list as an argument and adds all the items in the list to the set.

3. **Example:**
   ```
   # Create a list
   my_list = [1, 2, 3, 4]

   # Create a set
   my_set = set()

   # Add list items to the set
   my_set.update(my_list)

   # Print the set
   print(my_set)
   ```

4. **Output:**
   ```
   {1, 2, 3, 4}
   ```
