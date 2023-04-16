---
title: What is the best way to change all string values in a list of lists to integers?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use a list comprehension with the int() function to convert each string to an integer.
---

**Contents**

[TOC]

**Section 1: Create a List of Lists**

First, create a list of lists that contains strings that need to be converted to integers.

```
list_of_lists = [["1", "2", "3"], ["4", "5", "6"], ["7", "8", "9"]]
```

**Section 2: Use a For Loop**

Next, use a for loop to iterate through each list in the list of lists.

```
for list in list_of_lists:
    # Do something with each list
```

**Section 3: Convert Strings to Integers**

Inside the for loop, use a for loop to iterate through each string in the list. Then, use the int() function to convert each string to an integer.

```
for list in list_of_lists:
    for string in list:
        int_val = int(string)
```

**Section 4: Replace Strings with Integers**

Finally, replace the string with the integer value in the list of lists.

```
for list in list_of_lists:
    for idx, string in enumerate(list):
        list[idx] = int(string)
```

After running the code, the list of lists should look like this:

```
list_of_lists = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```
