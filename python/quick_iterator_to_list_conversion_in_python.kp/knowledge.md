---
title: The quickest method for transforming an iterator into a list is
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `list()` function to convert an iterator to a list in Python.
---

**Contents**

[TOC]

# Option 1: Using the list constructor

One of the easiest and fastest ways to convert an iterator to a list in Python is to use the built-in list() constructor. This method creates a new list object and adds each element from the iterator to the list. Here's an example:

```
my_iter = iter([1, 2, 3, 4, 5])
my_list = list(my_iter)
print(my_list)
```

Output:
```
[1, 2, 3, 4, 5]
```

In this example, we first create an iterator object `my_iter` that contains the elements `[1, 2, 3, 4, 5]`. We then convert this iterator to a list using the `list()` constructor, and store the result in `my_list`. Finally, we print out `my_list`.

# Option 2: Using a loop

Another way to convert an iterator to a list in Python is to use a loop. This method is simple and efficient, although it requires more code compared to the list constructor method. Here's an example:

```
my_iter = iter([1, 2, 3, 4, 5])
my_list = []
for element in my_iter:
    my_list.append(element)
print(my_list)
```

Output:
```
[1, 2, 3, 4, 5]
```

In this example, we first create the iterator object `my_iter` containing the elements `[1, 2, 3, 4, 5]`. We then create an empty list `my_list`, and use a for loop to iterate over each element in `my_iter`. For each element, we append it to `my_list`. Finally, we print `my_list`.


# Option 3: Using the extend method

If we already have a list object and want to add elements from an iterator to it, we can use the `extend()` method instead of the `append()` method. The `extend()` method takes an iterable as an argument and adds each element from the iterable to the list. Here's an example:

```
my_list = [1, 2, 3]
my_iter = iter([4, 5, 6])
my_list.extend(my_iter)
print(my_list)
```

Output:
```
[1, 2, 3, 4, 5, 6]
```

In this example, we first create the list `my_list` containing the elements `[1, 2, 3]`. We then create an iterator object `my_iter` containing the elements `[4, 5, 6]`. We use the `extend()` method to add each element from `my_iter` to `my_list`. Finally, we print `my_list`.


# Option 4: Using the slicing operator

The final option to convert an iterator to a list in Python is to use the slicing operator. This method works by slicing the entire iterator and creating a new list object containing all the sliced elements. Here's an example:

```
my_iter = iter([1, 2, 3, 4, 5])
my_list = list(my_iter[:])
print(my_list)
```

Output:
```
[1, 2, 3, 4, 5]
```

In this example, we first create the iterator object `my_iter` containing the elements `[1, 2, 3, 4, 5]`. We then convert the entire iterator to a list using the slicing operator, `my_iter[:]`. Finally, we print the resulting `my_list`. 

This method is similar to the list constructor method, and both are equally fast and efficient. However, the slicing method is useful when we need to get a subset of the iterator or skip some initial elements in the iterator.
