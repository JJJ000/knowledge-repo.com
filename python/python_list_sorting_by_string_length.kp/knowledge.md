---
title: Arranging a list in Python according to the character count of each string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the sorted() function with the key parameter set to len.
---

**Contents**

[TOC]

## Introduction ##

We can sort a Python list based on the length of the string which we will discuss in this tutorial using several methods.

## Method 1 - Using the sorted() method ##

One of the simplest ways to sort a Python list based on the length of the string is by using the sorted() method. We can pass an argument called key to the sorted() method which determines the sorting order. We can specify the key value as len.

```
# example list
words = ["apple", "cat", "bat", "dog", "banana"]

# sorting based on length
sorted_words = sorted(words, key=len)

# displaying the result
print(sorted_words)
```

Output:

```
['cat', 'bat', 'dog', 'apple', 'banana']
```

In the above example, we have sorted the list based on the length of the string by passing key value as the len function. 

## Method 2 - Using the sort() method ##

Another way to sort a Python list based on the length of the string is by using the sort() method. We can pass the same key value as the len function to the sort() method which will determine the sorting order.

```
# example list
words = ["apple", "cat", "bat", "dog", "banana"]

# sorting based on length
words.sort(key=len)

# displaying the result
print(words)
```

Output:

```
['cat', 'bat', 'dog', 'apple', 'banana']
```

In the above example, we have sorted the list based on the length of the string using the sort() method.

## Method 3 - Using lambda function ##

We can also use the lambda function to sort the list based on the length of the string. 

```
# example list
words = ["apple", "cat", "bat", "dog", "banana"]

# sorting based on length using lambda function
sorted_words = sorted(words, key=lambda x: len(x))

# displaying the result
print(sorted_words)
```

Output:

```
['cat', 'bat', 'dog', 'apple', 'banana']
```

In the above example, we have sorted the list based on the length of the string using the lambda function.

## Conclusion ##

In this tutorial, we discussed several ways to sort a Python list based on the length of the string. We used sorted() method, sort() method, and lambda function for sorting the list based on the length of the string.
