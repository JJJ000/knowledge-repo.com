---
title: The error message states that an integer was found when a string was expected for the first item in a sequence
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: This error occurs when trying to join a list of integers with a string using the join() method, which expects strings only.
---

**Contents**

[TOC]

Section 1: Understanding the Error Message

When an error message says "sequence item 0: expected string, int found", it indicates that a Python program tried to concatenate or join a string with an integer value. In Python, sequences like strings, lists, and tuples can be joined using the '+' operator. However, the '+' operator only works with elements of the same type. Therefore, if one of the elements is a string and another is an integer, Python will raise a "TypeError" with the message "sequence item 0: expected string, int found".

Section 2: Example of the Error

Consider the following Python code:

```python
message = "The answer is " + 42
print(message)
```

When executed, this code will raise a "TypeError" with the message "sequence item 0: expected string, int found". The reason is that the code is trying to join a string "The answer is " with an integer 42, which is not possible.

Section 3: Fixing the Error

To fix the "sequence item 0: expected string, int found" error, we need to ensure that the elements we are trying to join have the same type. In the example above, we can fix the error by converting the integer 42 to a string before joining it with the other string. 

```python
message = "The answer is " + str(42)
print(message)
```

The "str()" function in Python converts any value to a string. In this case, it will convert the integer 42 to the string "42". Now, when we join the two strings using the '+' operator, we get a valid string "The answer is 42".

Section 4: Conclusion

In this tutorial, we learned about the "sequence item 0: expected string, int found" error in Python. We saw that this error occurs when we try to join or concatenate a string with an integer value. We also saw how to fix this error by converting the integer value to a string before joining it with the other string. The "str()" function in Python can help us do this conversion.
