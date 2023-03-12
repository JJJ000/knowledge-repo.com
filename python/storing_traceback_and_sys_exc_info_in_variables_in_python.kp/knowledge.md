---
title: What is the method for storing traceback / sys.exc_info() values into a variable?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Simply assign the result of traceback.format\_exc() or sys.exc\_info() to a variable.
---

**Contents**

[TOC]

# Introduction
In Python, when an exception occurs, a traceback is displayed which shows the sequence of function calls that lead to the error. However, sometimes it is useful to save this information in a variable for further analysis or error reporting. In this article, we will discuss how to save traceback / sys.exc_info() values in a variable in Python.

# Using Exception Handling
One way to save traceback information is by using exception handling. We can catch the exception using a try-except block and then retrieve the traceback using the traceback module. Here is an example:

```
import traceback

try:
    # Code that may raise an exception
    1 / 0
except:
    # Get the traceback information
    tb_info = traceback.format_exc()
    
print(tb_info)
```

Output:
```
Traceback (most recent call last):
  File "<stdin>", line 3, in <module>
ZeroDivisionError: division by zero
```

# Using sys.exc_info()
Another way to retrieve traceback information is by using the sys.exc_info() function. This function returns a tuple of three values containing information about the last exception that occurred. Here is an example:

```
import sys

try:
    # Code that may raise an exception
    1 / 0
except:
    # Get the exception information
    exc_type, exc_value, exc_traceback = sys.exc_info()
    tb_info = traceback.format_exception(exc_type, exc_value, exc_traceback)
    
print(tb_info)
```

Output:
```
['Traceback (most recent call last):\n', '  File "<stdin>", line 3, in <module>\n', 'ZeroDivisionError: division by zero\n']
```

# Saving as a String or a List
Once we have the traceback information, we can save it as a string or as a list of strings. If we save it as a string, we can easily write it to a file or send it over the network. If we save it as a list of strings, we can use it to extract specific information about the traceback, such as the file name and line number where the exception occurred. Here is an example:

```
import traceback

try:
    # Code that may raise an exception
    1 / 0
except:
    # Get the traceback information
    tb_info = traceback.format_exc()
    
# Save as a string
with open('traceback.txt', 'w') as f:
    f.write(tb_info)
    
# Save as a list
tb_list = tb_info.split('\n')
print(tb_list[0])  # 'Traceback (most recent call last):'
print(tb_list[-3])  # 'ZeroDivisionError: division by zero'
```

Output:
```
Traceback (most recent call last):
ZeroDivisionError: division by zero
```

# Conclusion
In this article, we have discussed two ways to save traceback information in Python. We have also shown how to save the information as a string or a list for further analysis or error reporting. By saving traceback information, we can better understand and debug our programs in case of errors.
