---
title: What is the syntax for formatting a floating point number to a specific width in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the format() function with a format string specifying the desired width.
---

**Contents**

[TOC]

### Using the Format Method

The `format` method can be used to format a floating number to fixed width.

Syntax:

```
'{:width.precisionf}'.format(number)
```

Example:

```
'{:10.2f}'.format(3.1415926)
```

Output:

`    3.14`

### Using the Str.format Method

The `str.format` method can also be used to format a floating number to fixed width.

Syntax:

```
'{:width.precisionf}'.format(number)
```

Example:

```
'{:10.2f}'.format(3.1415926)
```

Output:

`    3.14`

### Using the F-Strings

F-strings can also be used to format a floating number to fixed width.

Syntax:

```
f'{number:width.precisionf}'
```

Example:

```
f'{3.1415926:10.2f}'
```

Output:

`    3.14`
