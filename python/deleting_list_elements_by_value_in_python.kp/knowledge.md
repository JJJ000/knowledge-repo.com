---
title: How can I remove an item from a list based on its value?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, you can use the list.remove(x) method to delete a list element by value in Python.
---

**Contents**

[TOC]

### Using a for loop

The simplest way to delete a list element by value in Python is to use a for loop. The following code snippet shows how to do this:

```python
my_list = [1, 2, 3, 4, 5]

value_to_delete = 3

for i in my_list:
    if i == value_to_delete:
        my_list.remove(i)

print(my_list) # [1, 2, 4, 5]
```

In the above code, we iterate through the list and check if the current element is equal to the value we want to delete. If it is, we call the `remove()` method on the list to remove that element.

### Using a list comprehension

Another way to delete a list element by value in Python is to use a list comprehension. The following code snippet shows how to do this:

```python
my_list = [1, 2, 3, 4, 5]

value_to_delete = 3

my_list = [x for x in my_list if x != value_to_delete]

print(my_list) # [1, 2, 4, 5]
```

In the above code, we use a list comprehension to create a new list that only contains elements that are not equal to the value we want to delete. This is a more concise and efficient way to delete a list element by value in Python.

### Using the filter() function

Finally, we can also use the `filter()` function to delete a list element by value in Python. The following code snippet shows how to do this:

```python
my_list = [1, 2, 3, 4, 5]

value_to_delete = 3

my_list = list(filter(lambda x: x != value_to_delete, my_list))

print(my_list) # [1, 2, 4, 5]
```

In the above code, we use the `filter()` function to create a new list that only contains elements that are not equal to the value we want to delete. This is another concise and efficient way to delete a list element by value in Python.
