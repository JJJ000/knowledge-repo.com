---
title: Determining the tally of boolean values that are true within a Python list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can count the number of True Booleans in a Python list using the count() method.
---

**Contents**

[TOC]

## Using a Loop

One simple and straightforward method to count the number of True Booleans in a Python List is to use a loop. Here is an example implementation:

```python
my_list = [True, False, True, True, False, False, True]

count = 0
for boolean in my_list:
    if boolean == True:
        count += 1

print(count)
```

Output:
```
4
```

Here, we iterate over each element in the list using a `for` loop, and check if the element is equal to `True`. If it is, we increment the `count` variable. Finally, we print the value of `count`, which represents the number of True Booleans in the list.


## Using the count() method

Another method to count the number of True Booleans in a Python List is to use the `count()` method. Here is an example implementation:

```python
my_list = [True, False, True, True, False, False, True]

count = my_list.count(True)

print(count)
```

Output:
```
4
```

Here, we simply call the `count()` method on our list, passing in the value we want to count (in this case, `True`) as an argument. The method returns the number of occurrences of that value in the list.


## Using list comprehension

We can use a list comprehension to shorten the loop method using list comprehension. Here is an example implementation:

```python
my_list = [True, False, True, True, False, False, True]

count = len([boolean for boolean in my_list if boolean == True])

print(count)
```

Output:
```
4
```

Here, we use list comprehension to create a new list of all the `True` values in `my_list`, and then take the `len()` of that list to get the count of `True` values.

## Using filter()

Another method to count the number of True Booleans in a Python List is to use the `filter()` method. Here is an example implementation:

```python
my_list = [True, False, True, True, False, False, True]

count = len(list(filter(lambda x: x, my_list)))

print(count)
```

Output:
```
4
```

Here, we use the `filter()` method with a lambda function that returns `True` for all truthy values. We then convert the resulting filter object into a list, and take the `len()` of that list to get the count of `True` values.
