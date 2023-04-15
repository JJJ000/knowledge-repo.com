---
title: Can you provide a procedure to convert the boolean value 'false' to 0 and 'true' to 1?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the int() function with the boolean value as an argument.
---

**Contents**

[TOC]

Intro
--------

In this tutorial, we will learn how to convert 'false' to 0 and 'true' to 1 in Python. For this purpose, we will use various methods available in Python. These methods are easy to use and applicable in different cases. So let's start.

Method 1: Using if-else statement
----------------------------------------

The easiest way to convert 'false' to 0 and 'true' to 1 in Python is by using the if-else statement. The if-else statement is a condition-based statement that checks whether the given condition is true or false. Based on the condition, it executes the corresponding code.

```python
s = 'false'
if s == 'false':
  s = 0
else:
  s = 1
print(s)
```
Output:
```python
0
```

In this code, first, we assign the value 'false' to the variable s. Then, we use the if-else statement to check whether the value of s is 'false' or not. If it is 'false', we assign it the value 0, and if not, we assign it the value 1. Finally, we print the value of s, which is 0 in this case.

Method 2: Using ternary operator
---------------------------------------

Another way to convert 'false' to 0 and 'true' to 1 in Python is by using the ternary operator. The ternary operator is a shorthand way of writing if-else statements.

```python
s = 'false'
s = 0 if s == 'false' else 1
print(s)
```

Output:
```python
0
```

In this code, we first assign 'false' to the variable s. Then, we use the ternary operator to check whether s is 'false' or not. If it is 'false', we assign s the value 0, and if not, we assign s the value 1. Finally, we print the value of s, which is 0 in this case.

Method 3: Using int() function
------------------------------------

The int() function is a built-in function in Python that converts a string to an integer. Since 0 and 1 are integers, we can use the int() function to convert 'false' to 0 and 'true' to 1.

```python
s = 'false'
s = int(s == 'true')
print(s)
```

Output:
```python
0
```

In this code, we first assign 'false' to the variable s. Then, we use the int() function to convert the boolean value (s=='true') to an integer. Since the boolean value is false, the integer value is 0. Finally, we print the value of s, which is 0 in this case.

Method 4: Using dict.get()
------------------------------ 

We can also use a dictionary to convert 'false' to 0 and 'true' to 1. First, we define a dictionary with 'false' and 'true' as keys and 0 and 1 as values, respectively. Then, we use the get() method of the dictionary to return the value corresponding to the key.

```python
s = 'false'
d = {'false': 0, 'true': 1}
s = d.get(s)
print(s)
```

Output:
```python
0
```

In this code, we first assign 'false' to the variable s. Then, we define a dictionary with the key-value pairs as described above. Finally, we use the get() method of the dictionary to return the value corresponding to the key. The value returned is 0 since the key is 'false'. Finally, we print the value of s, which is 0 in this case.

Conclusion
---------------

In this tutorial, we have learned how to convert 'false' to 0 and 'true' to 1 in Python using various methods. These methods are easy to use and applicable in different cases. Choose the method that suits your requirements and make your code more efficient.
