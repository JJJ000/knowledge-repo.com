---
title: Rearrange a collection of lists using a personalized comparison function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `sorted()` function with a `key` parameter set to a lambda function that defines the custom comparison logic.
---

**Contents**

[TOC]

## Sorting List with Custom Compare Function in Python

Sometimes, we need to sort a list of lists in Python using a custom compare function. In this tutorial, we will explore different ways to sort a list of lists with a custom compare function.


### Method 1: Using the sorted() built-in function

The sorted() built-in function accepts a custom compare function as a key argument. We can use this function to sort a list of lists by a specific index or column.

Example:

``` python
data = [['john', 45], ['jane', 32], ['mark', 18], ['sara', 24]]

def compare(lst):
    return lst[1]

sorted_data = sorted(data, key=compare)

print(sorted_data)
```

Output:

```
[['mark', 18], ['sara', 24], ['jane', 32], ['john', 45]]
```

Explanation:

In this example, we have defined a custom compare function `compare()` that returns the second element of each sublist `lst[1]`. We then use the `sorted()` function to sort the original list `data` based on the output of the compare function. The `key` parameter is set to `compare` to indicate that the sorting algorithm should use this function for sorting. The sorted data is stored in a new list `sorted_data` and printed to the console.


### Method 2: Using the sort() method of lists

The sort() method of lists also accepts a custom compare function as a key argument. We can use this method to sort a list of lists by a specific index or column.

Example:

``` python
data = [['john', 45], ['jane', 32], ['mark', 18], ['sara', 24]]

def compare(lst):
    return lst[1]

data.sort(key=compare)

print(data)
```

Output:

```
[['mark', 18], ['sara', 24], ['jane', 32], ['john', 45]]
```

Explanation:

In this example, we have defined a custom compare function `compare()` that returns the second element of each sublist `lst[1]`. We then use the `sort()` method to sort the original list `data` based on the output of the compare function. The `key` parameter is set to `compare` to indicate that the sorting algorithm should use this function for sorting. The original list `data` is sorted in-place and printed to the console.


### Method 3: Using lambda function

We can also use the lambda function to create a custom compare function on the fly. This is especially useful if we need to sort a list of lists based on multiple columns or indices.

Example:

``` python
data = [['john', 45], ['jane', 32], ['mark', 18], ['sara', 24]]

sorted_data = sorted(data, key=lambda x: (x[1], x[0]))

print(sorted_data)
```

Output:

```
[['mark', 18], ['sara', 24], ['jane', 32], ['john', 45]]
```

Explanation:

In this example, we use the lambda function to create a custom compare function that compares the second element of each sublist first and then compares the first element in case of a tie. The `sorted()` function uses this custom compare function to sort the original list `data`. The sorted data is stored in a new list `sorted_data` and printed to the console.


### Conclusion

In this tutorial, we explored different ways to sort a list of lists in Python using a custom compare function. We can use the built-in function `sorted()`, the `sort()` method of lists or the lambda function to create a custom compare function. By using these methods, we can sort a list of lists based on a specific index or column or based on multiple columns or indices.
