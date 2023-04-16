---
title: What is the best way to divide a list according to a specific criterion?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use a list comprehension to partition a list based on a condition in Python.
---

**Contents**

[TOC]

**Using List Comprehension**

1. Define the List:
   To start, define a list of items to be partitioned.

2. Define the Condition:
   Next, define the condition that will be used to partition the list.

3. Create the Partitions:
   Finally, use list comprehension to create two separate lists based on the condition. The syntax for this is as follows:
   ```
   list1 = [item for item in list if condition]
   list2 = [item for item in list if not condition]
   ```

**Using Loops**

1. Define the List:
   To start, define a list of items to be partitioned.

2. Define the Condition:
   Next, define the condition that will be used to partition the list.

3. Create the Partitions:
   Finally, use a loop to iterate over the list and create two separate lists based on the condition. The syntax for this is as follows:
   ```
   list1 = []
   list2 = []
   for item in list:
       if condition:
           list1.append(item)
       else:
           list2.append(item)
   ```
