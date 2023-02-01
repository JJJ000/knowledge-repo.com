---
title: Finding the position of the highest or lowest value in a list using max()/min()
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The index of the returned max or min item can be obtained using the index() method on the list.
---

**Contents**

[TOC]

#Section 1: max()

The max() function returns the item with the highest value in a list. To get the index of the returned max item, we can use the list.index() method.

#Section 2: Syntax

The syntax for using the list.index() method is as follows:

list.index(item)

#Section 3: Example

For example, if we have a list of numbers:

my_list = [1, 2, 3, 4, 5]

We can use the max() function to get the item with the highest value:

max_item = max(my_list)

And then use the list.index() method to get the index of the returned max item:

max_index = my_list.index(max_item)

#Section 4: Output

The output of the above code would be:

max_item = 5
max_index = 4
