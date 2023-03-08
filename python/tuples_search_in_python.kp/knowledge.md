---
title: Retrieve a tuple from a list containing the desired element
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use list comprehension or a for loop with if statement to iterate through the list of tuples and check if the element exists in each tuple.
---

**Contents**

[TOC]

## Section 1: Introduction

Python offers a lot of built-in functions to work with lists. One of the ways to store data in a list is by using tuples. A tuple is a collection of objects, similar to a list, but it is immutable. This means that once created, it cannot be modified. Suppose you have a list of tuples, and you want to search for an element in this list of tuples. In that case, Python offers several ways to do it. This article will discuss some of the ways to find an element in a list of tuples.

## Section 2: Using a for loop

One of the simplest ways to search for an element in a list of tuples is to iterate over the list using a for loop. In each iteration, we can check if the element we are searching for is present in the current tuple. Here's an example:

```
list_of_tuples = [('apple', 10), ('banana', 20), ('orange', 30)]
search_element = 'banana'

for item in list_of_tuples:
    if search_element in item:
        print(f"The element {search_element} exists in the tuple {item}")
        break
else:
    print(f"The element {search_element} does not exist in any tuple")
```

In this example, we first create a list of tuples with three elements. We then declare the variable `search_element` and initialize it with the value `'banana'`. We then iterate over the list of tuples using a for loop. In each iteration, we check if the search element exists in the current tuple. If it does, we print a message saying the element exists in that tuple and break out of the loop. If the loop completes without finding the element, we print a message saying the element does not exist in any tuple.

## Section 3: Using the filter function

Another way to search for an element in a list of tuples is to use the filter function along with a lambda function. Here's an example:

```
list_of_tuples = [('apple', 10), ('banana', 20), ('orange', 30)]
search_element = 'banana'

result_set = list(filter(lambda item: search_element in item, list_of_tuples))

if result_set:
    print(f"The element {search_element} exists in the tuple {result_set[0]}")
else:
    print(f"The element {search_element} does not exist in any tuple")
```

In this example, we first create a list of tuples with three elements. We then declare the variable `search_element` and initialize it with the value `'banana'`. We then use the filter function along with a lambda function to create a new list that contains only those tuples that have the search element. If the resulting list is not empty, we print a message saying the element exists in that tuple. Otherwise, we print a message saying the element does not exist in any tuple.

## Section 4: Conclusion

In this article, we discussed two ways to search for an element in a list of tuples in Python. The first way is to use a for loop to iterate over the list and check if the element exists in the current tuple. The second way is to use the filter function along with a lambda function to create a new list that contains only those tuples that have the search element. Both these methods are simple and can be easily implemented in Python.
