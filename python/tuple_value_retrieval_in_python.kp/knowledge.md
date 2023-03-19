---
title: Retrieving a single value from a tuple
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To get one value from a tuple in Python, simply use the index of the value inside the tuple, starting at 0.
---

**Contents**

[TOC]

Section 1: Understanding Tuples in Python
A tuple is an immutable collection of values enclosed in parentheses and separated by commas. This means that once a tuple is defined, its values cannot be changed unless a new tuple is created. Tuples are used to store related pieces of data that should not be changed individually.

Section 2: Accessing Values in Tuples
To access the values in a tuple, we can use indexing. This means that each value in the tuple has a unique index that starts at 0 for the first value. For example, if we have a tuple named `example_tuple` with values `(1, 2, 3)`, we can access each value using its index like this: 

```
example_tuple = (1, 2, 3)
print(example_tuple[0])
# Output: 1
print(example_tuple[1])
# Output: 2
print(example_tuple[2])
# Output: 3
```

Section 3: Getting One Value from a Tuple
In order to get one value from a tuple, we can simply access that value using its index. For example, if we have a tuple named `my_tuple` with values `(5, 10, 15, 20)`, and we want to get the value `10`, we use its index `1` like this:

```
my_tuple = (5, 10, 15, 20)
print(my_tuple[1])
# Output: 10
```

Section 4: Storing a Tuple Value in a Variable
If we want to use the value from a tuple in further operations, we can store it in a variable. This is done by assigning the value from the tuple using indexing to a new variable. For example, if we have a tuple named `person` with values `('John', 30, 'Male')`, and we want to store the age value `30` in a variable named `age`, we can do this:

```
person = ('John', 30, 'Male')
age = person[1]
print(age)
# Output: 30
```

Now we can use the `age` variable, which contains the value `30`, in further operations or calculations as needed.
