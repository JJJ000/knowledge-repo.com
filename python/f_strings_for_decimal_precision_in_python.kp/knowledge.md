---
title: Format fixed digits after the decimal point using f-strings
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: To format a float with two digits after the decimal, you can use an f-string such as f`{my\_float.2f}`.
---

**Contents**

[TOC]

### Using the Format Specifier

The most straightforward way to format digits after the decimal point with f-strings is to use the format specifier. This is done by including a colon (:) after the f-string, followed by the number of digits you want to appear after the decimal point.

For example, if you want to format a float to two digits after the decimal point, the syntax would be:

```python
f"{float_value:.2f}"
```

### Using the Round Function

If you want to format a float to a specific number of digits after the decimal point, you can use the round function. The syntax for this is:

```python
f"{round(float_value, n)}"
```

Where `n` is the number of digits after the decimal point.

### Using the Format Function

You can also use the format function to format a float to a specific number of digits after the decimal point. The syntax for this is:

```python
f"{format(float_value, '.nf')}"
```

Where `n` is the number of digits after the decimal point.

### Using the Str.Format Method

Finally, you can use the str.format method to format a float to a specific number of digits after the decimal point. The syntax for this is:

```python
f"{float_value:.{n}f}"
```

Where `n` is the number of digits after the decimal point.
