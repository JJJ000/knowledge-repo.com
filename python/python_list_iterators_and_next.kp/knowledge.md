---
title: The functioning of the Python list iterator and the usage of next(iterator) is being described
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: next(iterator) returns the next element from the Python list iterator, and raises StopIteration exception when it reaches the end of the list.
---

**Contents**

[TOC]

# Overview of Python list iterator

In Python, an iterator is an object that represents a stream of data. A list iterator is a type of iterator that is used to traverse a list in a sequential order. It provides a way to access the elements of a list without requiring the index of each element. 

To create an iterator object from a list in Python, we can use the `iter()` function. The `__next__()` method is called on the iterator object to get each successive element of the list. When there are no more elements in the list, the `StopIteration` exception is raised. 

# Using next(iterator) to access elements

Once an iterator has been created, we can retrieve its elements one at a time using the `next()` function. This function calls the `__next__()` method of the iterator and returns the next element in the list.

When there are no more elements in the list, the `next()` function raises a `StopIteration` exception. To avoid this exception, we can use the `for` loop to iterate through the entire list. 

Here is an example of using the `next()` function to access elements of a list iterator:

```
my_list = ['apple', 'banana', 'orange']
my_iterator = iter(my_list)

print(next(my_iterator))  # Output: 'apple'
print(next(my_iterator))  # Output: 'banana'
print(next(my_iterator))  # Output: 'orange'
print(next(my_iterator))  # Raises StopIteration exception
```

In this example, we have created an iterator object from the `my_list` list using the `iter()` function. We then use the `next()` function to retrieve each element of the list one at a time. When there are no more elements in the list, the `next()` function raises a `StopIteration` exception.

# Modifying the list during iteration

If we modify the list during iteration, it can lead to unexpected behavior. For example, if we add or remove elements from the list while iterating, the indices of the remaining elements will change.

Here is an example of modifying a list during iteration:

```
my_list = ['apple', 'banana', 'orange']
my_iterator = iter(my_list)

for fruit in my_iterator:
    print(fruit)
    if fruit == 'banana':
        my_list.remove(fruit)

# Output: 'apple', 'orange'
```

In this example, we have created an iterator object from the `my_list` list using the `iter()` function. We then use a `for` loop to retrieve each element of the list one at a time. We remove the element 'banana' from the list when it is encountered. 

However, this results in unexpected behavior as the `for` loop will continue iterating through the original list, which has now been modified. This will skip over the element 'orange', resulting in output that does not match the original list. 

# Conclusion

In this article, we have discussed the behavior of Python list iterators and the use of the `next()` function to retrieve elements. We have also seen that modifying a list during iteration can lead to unexpected behavior. It is important to be mindful of these behaviors when working with iterators and lists in Python.
