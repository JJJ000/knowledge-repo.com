---
title: How can a single line be used for an if-elif-else statement?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: It is possible to put an if-elif-else statement on one line in Python using a ternary operator.
---

**Contents**

[TOC]

Section 1: Introduction
Python’s if-elif-else statement is used for decision making. It evaluates multiple conditions and executes the code block associated with the first condition that is true. The if-elif-else statement has three parts – if, elif (else if), and else. In this tutorial, we will explore the possibility of putting an if-elif-else statement on a single line.

Section 2: Traditional way of writing an if-elif-else statement
Before we explore the possibility of putting an if-elif-else statement on a single line, let us first understand how it is traditionally written. Here’s an example:

```
num = 5

if num == 1:
    print("One")
elif num == 2:
    print("Two")
elif num == 3:
    print("Three")
else:
    print("None of the above")
```

In this example, we have used an if-elif-else statement to print the word representation of a number. The code checks if the value of `num` is equal to 1, 2, or 3, and prints the corresponding word. If the value of `num` is not equal to any of these numbers, it prints “None of the above”.

Section 3: Putting an if-elif-else statement on one line
Now, let’s explore the possibility of putting the above if-elif-else statement on a single line. Here’s how we can do it:

```
num = 5

print("One" if num == 1 else "Two" if num == 2 else "Three" if num == 3 else "None of the above")
```

In this one-liner code, we have used the conditional expression `x if condition else y`. This expression first evaluates the condition. If the condition is true, it returns `x`. If the condition is false, it returns `y`. We have used the conditional expression multiple times to check each condition in the if-elif-else statement.

Section 4: Conclusion
In conclusion, we have explored the possibility of putting an if-elif-else statement on a single line. While the traditional way of writing an if-elif-else statement is more readable and easier to understand, putting it on one line can be useful in some cases where we need to write a quick, concise code. However, this technique should be used with caution and only for simple if-elif-else statements. For complex statements with multiple conditions, the traditional way of writing an if-elif-else statement is more appropriate.
