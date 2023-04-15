---
title: Can one employ the word 'else' within a list comprehension?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Yes, it is possible to use `else` in a list comprehension in Python using ternary operators.
---

**Contents**

[TOC]

Yes, it is possible to use 'else' in a list comprehension in Python. Here's how you can do it:

## Using 'if-else' in a list comprehension

You can use an 'if-else' statement inside a list comprehension to return different values based on a condition. Here's an example:

```
numbers = [1, 2, 3, 4, 5, 6]
new_numbers = [n*2 if n%2==0 else n/2 for n in numbers]
print(new_numbers)
```

Output:
```
[0.5, 4, 1.5, 8, 2.5, 12]
```

In the example above, the list comprehension multiplies even numbers by 2 and divides odd numbers by 2.

## Using 'else' in a list comprehension

You can also use 'else' in a list comprehension to include a default value if a condition is not met. Here's an example:

```
numbers = [1, 2, 3, 4, 5, 6]
new_numbers = [n if n%2==0 else "odd" for n in numbers]
print(new_numbers)
```

Output:
```
['odd', 2, 'odd', 4, 'odd', 6]
```

In the example above, the list comprehension includes the string 'odd' for odd numbers and the number itself for even numbers.


## Using 'if-elif-else' in a list comprehension

You can also use 'if-elif-else' statements to return different values based on multiple conditions. Here's an example:

```
numbers = [1, 2, 3, 4, 5, 6]
new_numbers = ['even' if n%2==0 else 'odd' if n%3==0 else n for n in numbers]
print(new_numbers)
```

Output:
```
[1, 'even', 'odd', 'even', 'odd', 'even']
```

In the example above, the list comprehension returns 'even' for even numbers, 'odd' for numbers divisible by 3, and the number itself for other numbers.
