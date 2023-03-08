---
title: The order of the list returned by os.listdir() does not follow alphanumeric conventions
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: The order of non-alphanumeric list in os.listdir() in Python is not guaranteed and it may vary on different platforms.
---

**Contents**

[TOC]

Introduction

os.listdir() is a function in Python that helps to list all the files and directories in a particular directory on a system. The result obtained from os.listdir() is returned as a list. By default, the list is sorted based on the alphanumeric order of the filenames. However, in some use cases, we may want to sort the result in a different order, like the non-alphanumeric order. In this article, we will be discussing how to sort the list result from os.listdir() in non-alphanumeric order in Python.

Using sorted() and re.sub() functions

One way to sort the list result from os.listdir() in non-alphanumeric order is by using the sorted() and re.sub() functions. Here's an example:

```python
import os
import re

dir_path = "path/to/directory"
files_list = os.listdir(dir_path)
sorted_files_list = sorted(files_list, key=lambda x: (re.sub('[^0-9a-zA-Z]+', '', x), x))

print(sorted_files_list)
```

In the code above, we first import the os and re modules. We then specify the directory path whose list of files we want to sort. We use the os.listdir() function to list all the files in the directory and assign the result to the files_list variable. We then use the sorted() function to sort the files_list in non-alphanumeric order. We achieve this by specifying the key parameter to the sorted() function. The key parameter accepts a function that takes an argument and returns a value based on which the sorting will be done. In our case, we use a lambda function that takes an argument x and returns a tuple of two values. The first value is the alphanumeric part of the filename, which we obtain by removing all non-alphanumeric characters using the re.sub() function. The second value is the original filename as is. This ensures that we sort the files_list first based on their alphanumeric part and then based on their original order.

Using regular expressions and natural sorting techniques

Another way to sort the list result from os.listdir() in non-alphanumeric order is to use regular expressions and natural sorting techniques. Here's an example:

```python
import os
import re

dir_path = "path/to/directory"
files_list = os.listdir(dir_path)
sorted_files_list = sorted(files_list, key=lambda x: [int(c) if c.isdigit() else c.lower() for c in re.split('([0-9]+)', x)])

print(sorted_files_list)
```

In this code snippet, we again use os.listdir() to list all the files in the directory and assign the result to files_list. We then use the sorted() function to sort files_list in non-alphanumeric order using the key parameter. In the lambda function used for the key parameter, we use the re.split() function to split the filenames into two parts: numeric and non-numeric. We then convert the numeric part into integers and the non-numeric part into lowercase characters. This ensures that we sort the files_list based on natural sorting techniques for the numeric part and case-insensitive sorting techniques for the non-numeric part.

Conclusion

In this article, we discussed two methods to sort the list result from os.listdir() in non-alphanumeric order in Python. The first method uses sorted() and re.sub() functions, and the second method uses regular expressions and natural sorting techniques. These methods can help in cases where we want to sort the list of files based on a specific pattern or order.
