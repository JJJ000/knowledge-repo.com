---
title: Is it necessary to apply the int() function to all items in the list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use list comprehension to apply the int() function to every element in a list, like this [int(element) for element in my\_list].
---

**Contents**

[TOC]

Converting List Elements to Integer using int() Function in Python

### Introduction

In python, we can convert the list elements to integers using the built-in function int(). By calling the int() function on each element of the list, we can convert the elements to integers. In this article, we will discuss how to use the int() function to convert list elements to integers.


### Using for loop

One of the ways to convert list elements to integers using the int() function is by iterating through the list using a for loop. Here is the code snippet to illustrate this approach:

```
my_list = ['1', '2', '3', '4', '5']
int_list = []

for x in my_list:
    int_list.append(int(x))

print(int_list)
```

Output:

```
[1, 2, 3, 4, 5]
```

In the above code, we first defined a list 'my_list' with string elements. We then define an empty list 'int_list'. We iterate through the elements of 'my_list' using a for loop and convert each element to an integer using the int() function. Finally, we append the integer elements to the 'int_list' using the append() method. We then print the 'int_list' which contains the integer version of 'my_list'.


### Using map()

Another way to convert list elements to integers is by using the built-in function map(). Here is the code snippet to illustrate this method:

```
my_list = ['1', '2', '3', '4', '5']

int_list = list(map(int, my_list))

print(int_list)
```

Output:

```
[1, 2, 3, 4, 5]
```

In the above code, we first define the same list 'my_list' with string elements. We then use the map() function to convert each element of the list into an integer using the int() function. Finally, we convert the resultant map object to a list using the list() function and store it in 'int_list'. We then print the 'int_list' which contains the integer version of 'my_list'.


### Using list comprehension

Finally, we can also use a list comprehension to convert list elements to integers using the int() function. Here is the code to illustrate this method:

```
my_list = ['1', '2', '3', '4', '5']

int_list = [int(x) for x in my_list]

print(int_list)
```

Output:

```
[1, 2, 3, 4, 5]
```

In the above code, we first define the same list 'my_list' with string elements. We then use a list comprehension to convert each element of the list into an integer using the int() function. Finally, we store the resultant list in 'int_list'. We then print the 'int_list' which contains the integer version of 'my_list'.
