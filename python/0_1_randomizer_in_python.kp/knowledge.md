---
title: Can you generate a number between 0 and 1 that is random?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To generate a random number between 0 and 1 in Python, the random module can be used with the function random or uniform.
---

**Contents**

[TOC]

Section 1: Using the random module
To generate a random number between 0 and 1 in Python, we can make use of the random module. This module contains various functions that can be used to generate random numbers. 

Section 2: Using the random() function
The random module has a function called random() that can be used to generate a random float between 0 and 1. This function takes no arguments and returns a floating-point number. 

```python
import random

num = random.random()
print(num)
```

Output:
```
0.7121034979552747
```

Section 3: Generating a uniform distribution
We can also use the uniform() function of the random module to generate a random float between 0 and 1. This function takes two arguments - the start and end range of the uniform distribution. Since we want to generate a random number between 0 and 1, we can provide 0 and 1 as the start and end range. 

```python
import random

num = random.uniform(0, 1)
print(num)
```

Output:
```
0.8965631200988547
```

Section 4: Conclusion
Generating a random number between 0 and 1 in Python can be easily done using the random module's random() function or uniform() function. Both functions return a floating-point number between 0 and 1.
