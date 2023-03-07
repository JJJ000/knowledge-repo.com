---
title: What is the process for printing a Python dictionary one line at a time?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use a for loop to iterate over the key-value pairs of the dictionary and print each pair in a new line using f-string.
---

**Contents**

[TOC]

## Getting Started

Before we begin, it is important to understand what dictionaries are and how they are used in Python. 

Python dictionaries are used to store data in key-value pairs. The keys are unique identifiers that allow you to access the associated value quickly. You can think of a dictionary as a set of keys that point to associated values. 

## Printing a Dictionary Line by Line

Printing a dictionary line by line in Python is a common requirement in programming. There are various ways to achieve this, but we will discuss two methods - using a loop and using a list comprehension. 

### Method 1 - Using a Loop

One way to print a dictionary line by line is to use a loop. Here's the code:

```python
# Define a dictionary
my_dict = {"apple": 2, "banana": 4, "orange": 6}

# Loop through each key in the dictionary and print the key-value pairs
for key in my_dict:
    print(key, ":", my_dict[key])
```

In this code, we first define a dictionary `my_dict` that contains three key-value pairs. We then loop through each key in the dictionary using a `for` loop. Inside the loop, we print the key-value pairs using the `print` function. 

The output of this code will be:

```
apple : 2
banana : 4
orange : 6
```

### Method 2 - Using a List Comprehension

Another way to print a dictionary line by line is to use a list comprehension. Here's the code:

```python
# Define a dictionary
my_dict = {"apple": 2, "banana": 4, "orange": 6}

# Use a list comprehension to create a list of strings with key-value pairs
my_list = [f"{key}: {my_dict[key]}" for key in my_dict]

# Print the list line by line
print(*my_list, sep="\n")
```

In this code, we first define a dictionary `my_dict` that contains three key-value pairs. We then use a list comprehension to create a list of strings containing the key-value pairs. The `f` string formatting allows us to concatenate the key and value with a colon.

Finally, we print the list line by line using the `print` function with the `*` operator to unpack the list and the `sep` argument to specify the separator.

The output of this code will be the same as the previous method:

```
apple: 2
banana: 4
orange: 6
```

## Conclusion

Printing a dictionary line by line in Python is a common task in programming. In this guide, we discussed two methods of achieving this - using a loop and using a list comprehension. Both methods have their advantages and disadvantages, and you should choose the one that works best for your use case.
