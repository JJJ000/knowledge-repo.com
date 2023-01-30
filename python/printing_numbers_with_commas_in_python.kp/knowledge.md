---
title: What is the syntax for printing a number with commas as thousands separators?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the `format` function with the `,` flag to print a number with commas as thousands separators in Python.
---

**Contents**

[TOC]

# Using the Format Method

The `format` method can be used to print a number with commas as thousands separators. The syntax is as follows:

```
'{:,}'.format(number)
```

Where `number` is the number you would like to print with commas as thousands separators. 

For example, to print the number `1234567`, you would use the following code:

```
print('{:,}'.format(1234567))
```

The output of the above code would be: 

`1,234,567`

# Using the Locale Module

The `locale` module can also be used to print a number with commas as thousands separators. The syntax is as follows:

```
import locale
locale.setlocale(locale.LC_ALL, 'en_US.UTF-8')
locale.format("%d", number, grouping=True)
```

Where `number` is the number you would like to print with commas as thousands separators. 

For example, to print the number `1234567`, you would use the following code:

```
import locale
locale.setlocale(locale.LC_ALL, 'en_US.UTF-8')
print(locale.format("%d", 1234567, grouping=True))
```

The output of the above code would be: 

`1,234,567`
