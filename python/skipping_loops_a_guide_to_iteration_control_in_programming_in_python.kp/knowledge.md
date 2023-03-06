---
title: What is the method to bypass iterations in a loop?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `continue` keyword to skip iterations in a loop in Python.
---

**Contents**

[TOC]

# Introduction

Python's for loop is good for iterating through all the items in a list or a range. However, sometimes you may need to skip certain iterations based on certain conditions. In this article, we will discuss the different ways you can use to skip iterations in a loop in Python.

# Using the "continue" statement

The "continue" statement is used to skip the current iteration of a loop and move to the next iteration. When the "continue" statement is executed within a loop, the program skips over the remaining part of the loop and moves on to the next iteration.

The following example demonstrates how to use the "continue" statement in a loop:

```
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

In this example, the loop will iterate from 1 to 5. However, when the value of "i" is 3, the program will skip that iteration and move to the next iteration. Therefore, the output of the code will be:

```
1
2
4
5
```

# Using the "break" statement

The "break" statement is used to end a loop prematurely. When the "break" statement is executed within a loop, the loop terminates immediately, and the program continues to execute the code after the loop.

The following example demonstrates how to use the "break" statement in a loop:

```
for i in range(1, 6):
    if i == 3:
        break
    print(i)
```

In this example, the loop will iterate from 1 to 5. However, when the value of "i" is 3, the program will terminate the loop prematurely. Therefore, the output of the code will be:

```
1
2
```

# Using conditional statements to skip iterations

You can also use conditional statements to skip iterations in a loop. In this method, you use the if statement to check if a certain condition is met, and if it is, you skip the current iteration.

The following example demonstrates how to use conditional statements to skip iterations in a loop:

```
for i in range(1, 11):
    if i % 2 == 0:
        continue
    print(i)
```

In this example, the loop will iterate from 1 to 10. However, when the value of "i" is even, the program will skip that iteration and move to the next iteration. Therefore, the output of the code will be:

```
1
3
5
7
9
```

# Conclusion

In conclusion, you can skip iterations in a loop in Python using the "continue" statement, the "break" statement, or conditional statements. Depending on the situation, one of these methods may be more suitable than the others. Therefore, it is important to understand all of them and use them appropriately to achieve the desired result.
