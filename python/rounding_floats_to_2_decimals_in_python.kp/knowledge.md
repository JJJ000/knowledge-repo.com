---
title: Rounding floats to two decimal places
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Round the float to two decimal places using the round() function.
---

**Contents**

[TOC]

**Using the round() Function**

The round() function can be used to limit the number of decimal places for a float. The round() function takes two parameters, the number to be rounded and the number of decimal places to round it to.

Example:
```
x = 3.14159265
rounded = round(x, 2)
print(rounded)
```
Output:
```
3.14
```

**Using the format() Function**

The format() function can also be used to limit the number of decimal places for a float. The format() function takes two parameters, the number to be rounded and the format specification. The format specification should include the number of decimal places to round it to, indicated by the number of ‘#’ symbols after the decimal point.

Example:
```
x = 3.14159265
rounded = format(x, '.2f')
print(rounded)
```
Output:
```
3.14
```

**Using the % Operator**

The % operator can also be used to limit the number of decimal places for a float. The % operator takes two parameters, the number to be rounded and the format specification. The format specification should include the number of decimal places to round it to, indicated by the number of ‘f’ symbols after the decimal point.

Example:
```
x = 3.14159265
rounded = '%.2f' % x
print(rounded)
```
Output:
```
3.14
```

**Using the round() Method of the Decimal Class**

The round() method of the Decimal class can also be used to limit the number of decimal places for a float. The round() method takes two parameters, the number to be rounded and the number of decimal places to round it to.

Example:
```
from decimal import Decimal

x = 3.14159265
rounded = Decimal(x).quantize(Decimal('0.00'))
print(rounded)
```
Output:
```
3.14
```
