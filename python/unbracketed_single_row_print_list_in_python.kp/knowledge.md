---
title: Output the list in a single row without including any brackets
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the join() method to concatenate the list elements into a single string and specify a delimiter, such as a space or comma.
---

**Contents**

[TOC]

1. Creating a List
Before we can print a list without brackets in a single row in Python, we need to create a list. We can create a list by enclosing items in square brackets separated by commas. 
```python
my_list = ['apple', 'banana', 'orange', 'mango']
```

2. Printing a List Without Brackets
We can print a list without brackets by converting it to a string and then removing the brackets using string slicing. We can join the items of the list using a separator and then slice the string to remove the first and last character (which are the opening and closing brackets). 
```python
my_list = ['apple', 'banana', 'orange', 'mango']
separator = ', '
my_string = separator.join(my_list)
print(my_string[1:-1])
```

3. Using Print Function Parameters
We can also use the print function parameters to print a list without brackets. We can use the `sep` parameter to specify the separator and the `end` parameter to specify what should be printed after the last item. 
```python
my_list = ['apple', 'banana', 'orange', 'mango']
separator = ', '
print(*my_list, sep=separator, end='')
```

4. Using List Comprehension and Join Method
Another way to print a list without brackets in a single row in Python is to use list comprehension and the join method. We can use list comprehension to convert each item of the list to a string, and then use the join method to join the items without brackets. 
```python
my_list = ['apple', 'banana', 'orange', 'mango']
separator = ', '
my_string = ''.join([item + separator for item in my_list])[:-len(separator)]
print(my_string)
```

All of these methods will produce the same output: `apple, banana, orange, mango`
