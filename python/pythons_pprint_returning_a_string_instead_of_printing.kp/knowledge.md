---
title: Is there a way to make python's pprint function output a string instead of directly printing it?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `pprint` function with the `pformat` method from the `pprint` module.
---

**Contents**

[TOC]

Section 1: Introduction to pprint

Python's pprint module provides a way to pretty-print data structures to make them more readable. pprint is particularly useful when dealing with larger data structures such as dictionaries or lists, as it organizes and formats the data in a clear and concise way.

By default, pprint() prints the formatted data to the console. However, there may be times when you want to return the formatted data as a string instead of printing it to the console. In the next section, we will explore how to do this.

Section 2: Redirecting pprint output to a string

To redirect pprint output to a string, we can use the StringIO module from the io library. StringIO provides a way to work with string data as if it were a file-like object.

The following code demonstrates how to redirect pprint output to a string:

```
from pprint import pprint
from io import StringIO

data = {'name': 'John', 'age': 25, 'city': 'New York'}
output = StringIO()
pprint(data, output)
result = output.getvalue()
```

In the code above, we first import pprint and StringIO. We then create a sample dictionary called data.

We create a StringIO object called output, which will be used to capture the pprint output.

We then call pprint with the data and output arguments. This tells pprint to print the data to the output StringIO object instead of the console.

Finally, we get the value of the output object using getvalue() and store it in the variable result. This gives us the pprint output as a string.

Section 3: Conclusion

In this tutorial, we have seen how to redirect pprint output to a string. By using the StringIO module, we can capture the pprint output and store it in a string variable for further manipulation.

This technique can be particularly useful when dealing with larger data structures that may be difficult to read in their raw form. By using pprint and redirecting the output to a string, we can quickly and easily format the data in a readable way.

Overall, pprint is a powerful tool for working with complex data structures in Python, and its ability to redirect output to a string makes it even more versatile.
