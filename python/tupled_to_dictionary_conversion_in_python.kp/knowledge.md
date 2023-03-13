---
title: Convert a list of tuples into a dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: A dictionary in Python can be created from a list of tuples using dict() function or dictionary comprehension.
---

**Contents**

[TOC]

## Section 1: Understanding Tuples and Dictionaries

Before we move ahead to convert a list of tuples to a dictionary in Python, let us understand what tuples and dictionaries actually are.

### What are Tuples?
Tuples represent a sequence of elements which may have different data types. The elements in a tuple are enclosed in brackets and separated by commas. Tuples are immutable, which means that once a tuple is created, its values cannot be changed.

### What are Dictionaries?
Dictionaries are another type of collection in Python. The dictionary consists of a key-value pair, where both the key and value can be of any data type. In dictionaries, keys are unique, and values can be accessed using keys.

## Section 2: Converting List of Tuples to Dictionary

Now that we have a basic understanding of both tuples and dictionaries let's move ahead to convert a list of tuples to a dictionary. For this, we can use a loop, and for each tuple, we can create a key-value pair in the dictionary. 

### Step 1: Create a List of Tuples
Create a list of tuples. For instance, 

`list_of_tuples = [(1, 'apple'), (2, 'banana'), (3, 'orange')]`

### Step 2: Create an Empty Dictionary
Create an empty dictionary. We'll store our values into this dictionary. 

`my_dict = {}`

### Step 3: Loop Through the List of Tuples and Append to the Dictionary
We'll use a loop to iterate through the list of tuples, create a key-value pair, and add it to the dictionary. 

```
for key, value in list_of_tuples:
    my_dict[key] = value
```

### Step 4: Displaying Our Final Dictionary
Once all the tuples have been converted to key-value pairs in the dictionary, you can display the final dictionary using the print statement.

`print(my_dict)`

This will output: `{1: 'apple', 2: 'banana', 3: 'orange'}`


## Section 3: One-Liner Solution

Python is known for its minimalistic and concise code. We don't even have to use a loop to convert a list of tuples to a dictionary in Python. We can achieve the same result with a one-liner code. 

```
list_of_tuples = [(1, 'apple'), (2, 'banana'), (3, 'orange')]
my_dict = dict(list_of_tuples)
print(my_dict)
```

This one-liner code will produce the same output as Section 2. 


## Section 4: Conclusion

In conclusion, converting a list of tuples to a dictionary in Python is a simple task. We can achieve this using either a loop or a one-liner code. In any case, we first create an empty dictionary and then add key-value pairs to it using each tuple in the list.
