---
title: Adding identical strings to a collection of strings using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: You can use a list comprehension to append the same string to each string in the list.
---

**Contents**

[TOC]

## 1. Creating the list of strings

To begin with, we need a list of strings to which we can append the same string. We can create a simple list of strings using square brackets as shown below:

```
my_list = ['string1', 'string2', 'string3']
```

In this example, we have created a list called `my_list` that contains three strings. We will now proceed to append the same string to this list.


## 2. Appending the same string to the list

Once we have our list of strings, we can append the same string to each element of the list. We can do this using a for loop and the `append()` method as shown below:

```
for i in range(len(my_list)):
    my_list[i] += 'same_string'
```

In this example, we use a for loop to iterate over each element of the list. The `range()` function generates a sequence of numbers from 0 to the length of the list, which we can use to index into the list using square brackets. We then apply the `+=` operator to append the same string to each element of the list. Alternatively, we could have used the `append()` method as shown below:

```
for i in range(len(my_list)):
    my_list[i].append('same_string')
```

In this version, we use the `append()` method to add the same string as a new element to each string in the list.


## 3. Printing the updated list

Once we have appended the same string to each element of the list, we may wish to print the updated list to verify that the operation was successful. We can do this using a for loop to iterate over each element of the list and print it to the console as shown below:

```
for string in my_list:
    print(string)
```

In this example, we use a for loop to iterate over each element of the list. We then use the `print()` function to output each element of the list to the console.


## 4. Final code

Putting it all together, the final code to append the same string to a list of strings in Python looks like this:

```
my_list = ['string1', 'string2', 'string3']

for i in range(len(my_list)):
    my_list[i] += 'same_string'

for string in my_list:
    print(string)
```

This code creates a list of strings, appends the same string to each element of the list, and then prints the updated list to the console.
