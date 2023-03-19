---
title: What's the approach to splitting every item within a list by an integer?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use a list comprehension with the operation for division and the int as the divisor.
---

**Contents**

[TOC]

Section 1: Create a List and Integer

First, you will need to create a list of numbers and an integer to divide the elements by. For this example, we will use the following code:

```
my_list = [10, 20, 30, 40, 50]
divisor = 2
```

Here, we have created a list of five numbers (10, 20, 30, 40, 50) and an integer called `divisor` with a value of 2. 

Section 2: Use a For Loop to Iterate Through the List

Next, you will need to use a for loop to iterate through the list and divide each element by the integer. This can be done using the following code:

```
for i in range(len(my_list)):
    my_list[i] = my_list[i] / divisor

print(my_list)
```

This code loops through each element in the list using the `range()` function and the `len()` function to determine the length of the list. Then, it updates each element in the list by dividing it by the `divisor` integer. Finally, it prints the updated list to the console using the `print()` function.

Section 3: Use a List Comprehension to Divide Each Element

Alternatively, you can use a list comprehension to divide each element in the list by the integer. This can be done using the following code:

```
my_list = [num / divisor for num in my_list]

print(my_list)
```

This code uses a list comprehension to loop through each element in the list and update it by dividing it by the `divisor` integer. Finally, it prints the updated list to the console using the `print()` function.

Section 4: Use the map() Function to Divide Each Element

Another approach is to use the `map()` function to divide each element in the list by the integer. This can be done using the following code:

```
def divide_by(num):
    return num / divisor

my_list = list(map(divide_by, my_list))

print(my_list)
```

This code defines a function called `divide_by()` that takes in a number and returns that number divided by the `divisor` integer. Then, it uses the `map()` function to apply the `divide_by()` function to each element in the list. Finally, it prints the updated list to the console using the `print()` function.
