---
title: What is the way to obtain the negation or opposite of a boolean in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the not operator before the Boolean value to get its negation in Python.
---

**Contents**

[TOC]

# Introduction

In this tutorial, we will explore how to get the opposite (or negation) of a Boolean in Python.

## Using the not operator

The simplest way to get the opposite of a Boolean value in Python is to use the not operator. The not operator is a unary operator, which means it takes only one operand.

Here's an example:

```python
value = True
opposite = not value
print(opposite)
```

Output:

```
False
```

In the example above, we use the not operator to get the opposite of the Boolean value `True`. The result of the operation is assigned to the variable `opposite`, which is then printed.

## Using the xor operator

Another way to get the opposite of a Boolean value is to use the xor operator. The xor operator is a binary operator, which means it takes two operands.

Here's an example:

```python
value = True
opposite = value ^ True
print(opposite)
```

Output:

```
False
```

In the example above, we use the xor operator to get the opposite of the Boolean value `True`. The `^` operator returns `True` if the two operands are different, and `False` if they are the same. In this case, the first operand is `True` and the second operand is also `True`. Therefore, the result of the operation is `False`.

## Using the != operator

A third way to get the opposite of a Boolean value is to use the != operator. The != operator is a binary operator, which means it takes two operands.

Here's an example:

```python
value = True
opposite = value != True
print(opposite)
```

Output:

```
False
```

In the example above, we use the != operator to get the opposite of the Boolean value `True`. The != operator returns `True` if the two operands are different, and `False` if they are the same. In this case, the first operand is `True` and the second operand is also `True`. Therefore, the result of the operation is `False`.
