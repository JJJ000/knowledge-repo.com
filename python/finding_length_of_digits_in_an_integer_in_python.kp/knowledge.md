---
title: What is the length of the number of digits in an integer?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The length of digits in an integer can be found using the built-in function len() on the string representation of the integer.
---

**Contents**

[TOC]

# Section 1: Using a While Loop

The following code will iterate through the integer and count the number of digits.

```python
n = int(input("Enter a number: "))
count = 0

while n > 0:
    n = n // 10
    count += 1

print("The number of digits is:", count)
```

# Section 2: Using a For Loop

The following code will iterate through the integer and count the number of digits.

```python
n = int(input("Enter a number: "))
count = 0

for i in range(n):
    n = n // 10
    count += 1

print("The number of digits is:", count)
```

# Section 3: Using the Len Function

The following code will use the len() function to count the number of digits.

```python
n = int(input("Enter a number: "))

count = len(str(n))

print("The number of digits is:", count)
```

# Section 4: Using the Log Function

The following code will use the log() function to count the number of digits.

```python
import math

n = int(input("Enter a number: "))

count = math.floor(math.log10(n) + 1)

print("The number of digits is:", count)
```
