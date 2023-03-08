---
title: What is the process of generating a dictionary where the keys originate from a list and the values are set to (for instance) zero by default?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use a dictionary comprehension with the list as the keys and `0` as the default value for all values in the dictionary.
---

**Contents**

[TOC]

1. Create a List of Keys:
    ```python
    my_list = ['a', 'b', 'c', 'd']
    ```

2. Using a dictionary comprehension with a default value of 0:
    ```python
    my_dict = {key: 0 for key in my_list}
    ```
3. Printing the resulting dictionary:
    ```python
    print(my_dict)
    ```
Output:
```
{'a': 0, 'b': 0, 'c': 0, 'd': 0}
```

Explanation:

1. First, we create a list of keys that we want to use in our dictionary. In this example, we created a simple list of four strings called `my_list`.

2. Then, we use a dictionary comprehension to create a dictionary from our list with each key having a value of 0. We do this by iterating over each item in the list and creating a key-value pair with the key as the item and the value as 0. The resulting dictionary is stored in the variable `my_dict`.

3. Finally, we print the resulting dictionary to the console using the `print()` function. The output shows that each key in the dictionary has a corresponding value of 0, as expected.
