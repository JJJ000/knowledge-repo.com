---
title: The counter for a for loop in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Python loop counter can be created using the built-in function enumerate() in a for loop.
---

**Contents**

[TOC]

Section 1: Introduction
A loop counter is a variable that counts the number of iterations a loop has executed. In Python, we can use the range() function to create a loop and also define a variable that will serve as our loop counter. The counter variable is updated on each iteration of the loop.

Section 2: Using a for Loop with a Counter Variable
A for loop is an iterative loop that is used to execute a block of code a fixed number of times. The loop counter is used to keep track of the number of iterations that have been executed. For example, the following code uses a for loop with a counter variable (i) to print the numbers 0 to 4:

```python
for i in range(5):
    print(i)
```

Output:
```
0
1
2
3
4
```

In the above example, i is the loop counter variable. It is initialized to 0 and incremented by 1 on each iteration of the loop. This loop will execute five times, with i taking on the values 0, 1, 2, 3, and 4.

Section 3: Using the Counter Variable in Loop Logic
We can use the loop counter variable in the logic of a loop to perform actions based on the number of iterations executed. For example, consider the following code that uses a for loop with a counter variable to calculate the sum of the even numbers from 0 to 10:

```python
sum = 0
for i in range(11):
    if i % 2 == 0:
        sum += i
print(sum)
```

Output:
```
30
```

In the above example, i is the loop counter variable. We use the modulus operator (%) to check if i is an even number. If i is even, we add it to the sum variable. This loop will execute 11 times, with i taking on the values 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, and 10.

Section 4: Conclusion
Python loop counter variables are essential when working with loops. They allow us to keep track of the number of iterations that have been executed and perform actions based on the number of iterations executed. We can use loop counter variables in both the initialization of the loop and in the logic of the loop itself.
