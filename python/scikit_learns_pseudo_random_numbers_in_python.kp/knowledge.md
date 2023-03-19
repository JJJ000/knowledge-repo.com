---
title: In scikit learn, the term "pseudo-random number" or "random state" can be used interchangeably
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Random state or pseudo-random number is used to set a seed value to generate the same sequence of random numbers each time the code is run in Scikit learn in Python.
---

**Contents**

[TOC]

Section 1: Introduction

Randomness is essential in many fields ranging from scientific research to game development. In Scikit learn, the pseudo-random number generator is used for sampling data and initializing certain machine learning algorithms. However, setting the seed for the random number generator is crucial for reproducibility in research. This article will discuss the use of the random state function in scikit-learn.

Section 2: What is a random state?

A random state is an initial value that is fed to the pseudo-random number generator. This initial value determines the sequence of random numbers generated. By setting the seed to the same value, the same sequence of random numbers can be reproduced. This is important in machine learning when data needs to be split into training and testing sets, and the model needs to be evaluated. By setting a random state, the split and evaluation process is reproducible.

Section 3: How to implement a random state in scikit-learn

The random_state parameter can be set in various scikit-learn functions that involve pseudo-random number generation. For example, in the train_test_split function, the random_state parameter can be set to control the random splitting of the training and testing datasets. Here is an example of how to set a random state in the train_test_split function:

```
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

In this example, the random_state parameter is set to 42, ensuring that the same split of the data into training and testing sets is produced each time the code is run.

Section 4: Conclusion

In conclusion, the random state function is a crucial component of reproducibility in machine learning research. By setting the random state, a sequence of pseudo-random numbers is produced that can be reproduced, allowing others to replicate findings and build upon previous research. Ensuring reproducibility is essential for the advancement of science in general and machine learning, in particular, to make reliable and efficient models.
