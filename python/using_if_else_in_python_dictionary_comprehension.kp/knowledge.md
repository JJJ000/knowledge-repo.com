---
title: In what way can if/else be employed in a dictionary comprehension?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: It is not possible to use if/else in a dictionary comprehension directly, but you can use a ternary operator as the value expression.
---

**Contents**

[TOC]

Section 1: Overview
To use an if/else statement in a dictionary comprehension in Python, you need to define the logic for the if/else statement and then incorporate it into the dictionary comprehension. There are several ways to do this, depending on the specific use case.

Section 2: Using a Ternary Operator
One way to use if/else in a dictionary comprehension is to use a ternary operator. For example, if you have a dictionary `my_dict` and want to create a new dictionary where each key is the same as the original dictionary, and the value is the original value if it is even, and the value divided by two if it is odd. You could use the following code:

```
my_dict = {1: 5, 2: 4, 3: 7, 4: 8}
new_dict = {key: (value if value % 2 == 0 else value/2) for key, value in my_dict.items()}
print(new_dict)
# Output: {1: 2.5, 2: 4, 3: 3.5, 4: 8}
```

In the above code, the ternary operator `(value if value % 2 == 0 else value/2)` is used to determine whether the value should be kept as is or divided by two.

Section 3: Using a Lambda Function
Another way to use if/else in a dictionary comprehension is to use a lambda function. For example, if you have a list of numbers and want to create a dictionary where each key is a number in the list, and the value is 'even' if the number is even, and 'odd' if the number is odd. You could use the following code:

```
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
new_dict = {num: (lambda: 'even' if num % 2 == 0 else 'odd')() for num in my_list}
print(new_dict)
# Output: {1: 'odd', 2: 'even', 3: 'odd', 4: 'even', 5: 'odd', 6: 'even', 7: 'odd', 8: 'even', 9: 'odd'}
```

In the above code, a lambda function is used to determine whether the key is even or odd.

Section 4: Conclusion
Using if/else in a dictionary comprehension in Python is a useful way to create new dictionaries based on logic. Whether you choose to use a ternary operator or a lambda function, the key is to define the logic first and then incorporate it into the dictionary comprehension.
