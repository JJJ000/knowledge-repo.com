---
title: Does Python have a function for calculating ncr in mathematics?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Yes, there is a math nCr function in Python which is available in the `math` module.
---

**Contents**

[TOC]

Yes, there is a math nCr function in python. 

# Section 1 - Explanation of nCr

nCr is a mathematical function that calculates the number of possible combinations of n items taken r at a time. It is also known as the binomial coefficient or the combination function.

The formula for nCr is: nCr = n! / r! (n - r)! 

Where n! is the factorial of n, which is the product of all positive integers up to n. 

# Section 2 - Using the math module in python

Python has a built-in math module that includes a variety of mathematical functions, including the nCr function.

To use the nCr function in python, you first need to import the math module:

``` python
import math
```

Then, you can call the nCr function using math.comb(n,r), where n is the total number of items and r is the number of items being chosen. 

``` python
# calculate the number of possible combinations of 5 items taken 3 at a time
combinations = math.comb(5,3)
print(combinations) # output: 10
```

# Section 3 - Alternative Implementations

If you don't have the math module available or want to implement nCr yourself, you can do so using the formula above:

``` python
# define a factorial function
def factorial(n):
  if n == 0:
    return 1
  else:
    return n * factorial(n-1)

# define an nCr function
def nCr(n,r):
  return factorial(n) / (factorial(r) * factorial(n-r))

# calculate the number of possible combinations of 5 items taken 3 at a time
combinations = nCr(5,3)
print(combinations) # output: 10.0
```

# Section 4 - Conclusion

In conclusion, there is a math nCr function in python, which is part of the built-in math module. You can also implement nCr yourself using the formula or create a factorial function to be used in the formula.
