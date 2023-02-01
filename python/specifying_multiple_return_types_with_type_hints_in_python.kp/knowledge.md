---
title: What is the syntax for declaring multiple return types using type-hints?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: In Python, multiple return types can be specified using type-hints by using Union[type1, type2, ...] as the return type.
---

**Contents**

[TOC]

## Using Union

Type hints can be used to specify multiple return types using the `Union` type. `Union` is used to indicate that the return type can be one of the types specified in the `Union` argument. 

For example, if a function returns either a `str` or `int` type, the type hint would be `Union[str, int]`:

```python
def example_function() -> Union[str, int]:
    ...
```

## Using Any

The `Any` type can also be used to indicate that the return type can be any type. This is useful when the return type is not known or can change.

For example, if a function can return any type, the type hint would be `Any`:

```python
def example_function() -> Any:
    ...
```

## Using Tuple

The `Tuple` type can be used to indicate that the return type can be a tuple of any types. This is useful when the return type is a tuple of multiple types.

For example, if a function returns a tuple of `str` and `int` types, the type hint would be `Tuple[str, int]`:

```python
def example_function() -> Tuple[str, int]:
    ...
```

## Using Literal

The `Literal` type can be used to indicate that the return type can be one of the specified literal values. This is useful when the return type is a literal value, such as a boolean or a string.

For example, if a function returns either `True` or `False`, the type hint would be `Literal[True, False]`:

```python
def example_function() -> Literal[True, False]:
    ...
```
