---
title: A csv file created using Python will have empty lines between each row
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, by default Python`s csv library adds a blank line between each row when writing to a CSV file.
---

**Contents**

[TOC]

# Section 1: Causes

The most common cause of blank lines appearing between rows in a CSV file written with Python is due to the use of the `print()` function. When the `print()` function is used, it automatically adds a blank line after each row that is printed. This can be avoided by using the `write()` function instead, which does not add any extra whitespace when writing to the file.

# Section 2: Solutions

The simplest solution to this problem is to avoid using the `print()` function when writing to a CSV file. Instead, use the `write()` function to directly write the data to the file. This will ensure that there are no extra blank lines added between rows.

Another solution is to use the `csv.writer()` class in the Python `csv` module. This class provides a number of options for controlling how data is written to the file, including the ability to specify whether or not to include blank lines between rows.

# Section 3: Alternatives

If the `csv.writer()` class is not an option, another alternative is to use the `str.join()` method to combine the data into a single string before writing it to the file. This method allows you to specify a delimiter character (such as a comma) which will be used to separate the data and avoid the addition of extra blank lines.

# Section 4: Conclusion

In conclusion, blank lines appearing between rows in a CSV file written with Python are usually caused by the use of the `print()` function. This can be avoided by using the `write()` function instead, or by using the `csv.writer()` class or the `str.join()` method.
