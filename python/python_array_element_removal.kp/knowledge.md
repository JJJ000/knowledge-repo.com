---
title: What is the method to delete a particular element from an array with the help of python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `remove` method to remove a specific element from an array in Python.
---

**Contents**

[TOC]

## Introduction
Arrays are a useful data structure in Python that allow you to store and manipulate multiple values in a single variable. However, at times, you may need to remove a specific element from an array. In this tutorial, we will explore how to remove a specific element from an array using Python.

## Using the remove() method
One of the easiest ways to remove a specific element from an array is to use the remove() method. The remove() method removes the first occurrence of a specified element from the array.

```python
arr = [1, 2, 3, 4, 5]
arr.remove(3)
print(arr)
```

Output:
```
[1, 2, 4, 5]
```

In the above code, we created an array with five elements. We then called the remove() method and passed in the value `3`. The remove() method removed the first occurrence of `3` from the array, which was at index `2`.

## Using a for loop
Another way to remove a specific element from an array is to use a for loop. We can iterate through the array and check if each element matches the value we want to remove. If we find a match, we can use the pop() method to remove the element.

```python
arr = [1, 2, 3, 4, 5]
remove_value = 3
for i in range(len(arr)):
    if arr[i] == remove_value:
        arr.pop(i)
        break
print(arr)
```

Output:
```
[1, 2, 4, 5]
```

In the above code, we again created an array with five elements. We then set `remove_value` to `3` and looped through the array. We checked if the current element in the loop matched `remove_value`. If it did, we used the pop() method to remove the element at the current index. We then used the break statement to exit the loop after the first match was removed.

## Using list comprehension
List comprehension is a concise way of creating a list or array from an existing list or array. We can use list comprehension to create a new array that excludes the element we want to remove.

```python
arr = [1, 2, 3, 4, 5]
remove_value = 3
new_arr = [x for x in arr if x != remove_value]
print(new_arr)
```

Output:
```
[1, 2, 4, 5]
```

In the above code, we created an array with five elements again. We set `remove_value` to `3` and created a new array using list comprehension. The new array includes all elements from the original array that do not match `remove_value`.

## Conclusion
In this tutorial, we explored three different ways to remove a specific element from an array in Python. The remove() method is the simplest, while using a for loop and list comprehension offer more flexibility. Choose the method that best suits your needs and use case.
