---
title: Is there a way to eliminate several items from a list using a single statement?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use a list comprehension with a conditional statement to filter out the items to be removed in a single expression.
---

**Contents**

[TOC]

# Introduction
Python provides a lot of built-in methods for manipulating lists. One of the most common tasks in list operations is removing one or more items from a list. In some cases, we need to remove multiple items from a list at once. This tutorial explores how to remove multiple items from a list in just one statement in Python, using examples and explanations.

# Using List Comprehension
One way to remove multiple items from a list in one statement is to use list comprehension. We can create a new list by iterating through the original list and excluding the elements to be removed.

Here's an example code snippet that demonstrates this approach:

```
# creating the list
my_list = ['apple', 'banana', 'coconut', 'dates', 'eggplant', 'figs']

# specifying the items to be removed
items_to_remove = ['banana', 'dates', 'eggplant']

# removing the items in one statement using list comprehension
new_list = [item for item in my_list if item not in items_to_remove]

# printing the new list
print(new_list)
```

In the above code, we first initialize a list called `my_list`. We then specify the items to be removed in a separate list called `items_to_remove`. Next, we use a list comprehension expression to create a new list that contains all the elements of `my_list` except the ones to be removed. Finally, we print the new list.

# Using the filter function
Another way to remove multiple items from a list in one statement is to use the `filter()` function. The `filter()` function takes a function and a sequence as inputs, and returns an iterator with the elements from the sequence for which the function returns `True`. We can define a lambda function that returns `False` for the items to be removed, and apply it to the original list using the `filter()` function.

Here's an example code snippet that demonstrates this approach:

```
# creating the list
my_list = ['apple', 'banana', 'coconut', 'dates', 'eggplant', 'figs']

# specifying the items to be removed
items_to_remove = ['banana', 'dates', 'eggplant']

# removing the items in one statement using the filter() function
new_list = list(filter(lambda x: x not in items_to_remove, my_list))

# printing the new list
print(new_list)
```

In the above code, we first initialize a list called `my_list`. We then specify the items to be removed in a separate list called `items_to_remove`. Next, we define a lambda function that returns `True` for all the elements that are not in `items_to_remove`. We apply this lambda function to the original list using the `filter()` function, and convert the resulting iterator to a list. Finally, we print the new list.

# Conclusion
In this tutorial, we explored two approaches for removing multiple items from a list in just one statement in Python. We looked at using list comprehension and the `filter()` function, with examples and explanations. These approaches can help simplify our code and make it more readable and concise. However, it is important to note that these methods create new lists, which may not be efficient for large datasets.
