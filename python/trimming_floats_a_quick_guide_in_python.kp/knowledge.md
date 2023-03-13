---
title: What is the method for shortening decimal numbers?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To truncate float values in Python, use the `int()` or `math.trunc()` functions.
---

**Contents**

[TOC]

1. Using string formatting:

One way to truncate float values in Python is to use string formatting technique. We can format a float value and specify the number of decimal places we want to keep. We can achieve this using the "{:.nf}" syntax, where "n" is the desired number of decimal places. Here's an example:

```python
num = 3.14159265359
trunc_num = "{:.2f}".format(num)
print(trunc_num) # Output: 3.14
```

2. Using round() method:

Another way to truncate float values in Python is to use the built-in round() method. We can pass a float value and specify the number of decimal places we want to keep. Here's an example:

```python
num = 3.14159265359
trunc_num = round(num, 2)
print(trunc_num) # Output: 3.14
```

3. Truncating towards zero using math.trunc():

If we want to truncate float values towards zero, we can use the math.trunc() method. It returns the integer value of the given float by removing the fractional part. Here's an example:

```python
import math
num = 3.14159265359
trunc_num = math.trunc(num)
print(trunc_num) # Output: 3
```

4. Truncating using int():

We can also truncate float values using the int() method. It removes the fractional part of the float and returns the integer value. However, we should note that this method only truncates towards zero. Here's an example:

```python
num = 3.14159265359
trunc_num = int(num)
print(trunc_num) # Output: 3
```

Overall, there are multiple ways to truncate float values in Python, and the method will depend on the specific use case and rounding requirements.
