---
title: Does a function similar to zip exist that adds padding to match the longest length?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Yes, the itertools.zip\_longest() function can be used in Python to zip two or more iterables together and pad the shorter ones with a specified fill value to match the length of the longest iterable.
---

**Contents**

[TOC]

Yes, there is a zip-like function that pads to the longest length in Python. It is called zip_longest() and is part of the itertools module. 

Section 1: Overview of zip_longest()
The zip_longest() function allows you to iterate over several iterables as if they were combined into tuples like the regular zip() function. However, if one of the iterables is shorter than the others, the zip_longest() function will pad it with a specified value (by default, None) so that all iterables have the same length. 

Section 2: How to Use zip_longest()
The syntax for using zip_longest() is similar to zip(). It takes two or more iterables as arguments and returns an iterator that produces tuples of the combined elements from each iterable. If you want to specify a padding value other than None, you can pass it as the fillvalue argument. 

Here's an example usage of the zip_longest() function that pads the second iterable with the value 0:

```python
from itertools import zip_longest

a = [1, 2, 3]
b = [4, 5]

for x, y in zip_longest(a, b, fillvalue=0):
    print(x, y)

# Output: 
# 1 4
# 2 5
# 3 0
```

As you can see, the zip_longest() function combines the elements of list `a` with the elements of list `b`. Since `b` is shorter than `a`, it is padded with the value 0 so that both lists have the same length. 

Section 3: Other Arguments of zip_longest()
In addition to the fillvalue argument, the zip_longest() function also has the following optional arguments:

1. `*args`: Specifies the iterables to be combined. 

2. `fillvalue`: Specifies the value to use for padding. The default value is None. 

3. `missing`: Specifies how missing values should be represented in the output tuples. The default behavior is to use the fillvalue argument, but you can also choose to raise an error or use a different marker value. 

4. `left_fillvalue`: Specifies the value to use for padding on the left side of the shortest iterable. The default value is None. 

5. `right_fillvalue`: Specifies the value to use for padding on the right side of the shortest iterable. The default value is None. 

Section 4: Conclusion
The zip_longest() function in Python's itertools module is a useful tool for combining iterables and padding unequal lengths. It allows you to easily iterate over multiple sequences as if they were combined into tuples, while handling any missing values with customizable padding.
