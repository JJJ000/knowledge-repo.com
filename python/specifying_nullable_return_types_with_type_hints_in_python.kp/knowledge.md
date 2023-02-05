---
title: What is the syntax for indicating a "nullable" return type with type hints?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The `nullable` return type can be specified using the typing.Optional[T] type hint in Python.
---

**Contents**

[TOC]

### Using the typing Module

The `typing` module in Python provides a set of type hints to help developers express the expected types of values in their code. To indicate that a function can return `None`, the `typing.Optional` type can be used.

For example, if a function is expected to return an `int` or `None`, the following type hint can be used:

```python
def my_function() -> typing.Optional[int]:
    # ...
```

### Using the Union Type

The `typing.Union` type can also be used to indicate that a function can return `None`. This type allows for specifying multiple types for a single type hint.

For example, if a function is expected to return an `int` or `None`, the following type hint can be used:

```python
def my_function() -> typing.Union[int, None]:
    # ...
```

### Using the Literal Type

The `typing.Literal` type can also be used to indicate that a function can return `None`. This type allows for explicitly specifying a single value that is allowed for a type hint.

For example, if a function is expected to return an `int` or `None`, the following type hint can be used:

```python
def my_function() -> typing.Literal[int, None]:
    # ...
```

### Using the NoneType

Finally, the `typing.NoneType` type can also be used to indicate that a function can return `None`. This type allows for explicitly specifying that the only allowed value is `None`.

For example, if a function is expected to return an `int` or `None`, the following type hint can be used:

```python
def my_function() -> typing.NoneType:
    # ...
```
