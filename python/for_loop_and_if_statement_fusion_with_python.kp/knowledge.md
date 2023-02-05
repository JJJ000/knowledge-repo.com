---
title: Writing a for-loop that includes an if-statement in a pythonic style
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use a list comprehension to combine a for-loop and if-statement.
---

**Contents**

[TOC]

### Using List Comprehension 
List comprehension is a concise way to combine a for loop and an if statement. It is a single line that creates a list based on existing iterable. 

Syntax: 
```
[expression for item in list if condition]
```

Example: 
```
numbers = [1, 2, 3, 4, 5]

even_numbers = [num for num in numbers if num % 2 == 0]

print(even_numbers)  # Output: [2, 4]
```

### Using Filter
The `filter()` function is used to filter out elements from a given list that satisfy a certain condition.

Syntax:
```
filter(function, iterable)
```

Example:
```
numbers = [1, 2, 3, 4, 5]

even_numbers = filter(lambda x: x % 2 == 0, numbers)

print(list(even_numbers))  # Output: [2, 4]
```

### Using Generator Expression
Generator expressions provide a more memory-efficient way to create a list in a single line.

Syntax:
```
(expression for item in list if condition)
```

Example:
```
numbers = [1, 2, 3, 4, 5]

even_numbers = (num for num in numbers if num % 2 == 0)

print(list(even_numbers))  # Output: [2, 4]
```
