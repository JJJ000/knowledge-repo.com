---
title: What is the best way to obtain the first n elements from a generator or list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: To take the first N items from a generator or list in Python, use the slicing notation [N].
---

**Contents**

[TOC]

# Section 1: Taking the First N Items from a Generator

To take the first N items from a generator, you can use the `itertools.islice` function. The `islice` function takes a generator as its first argument, and the second argument is a `stop` value that specifies the number of items you want to take from the generator.

For example, if you have a generator `my_gen` and you want to take the first 5 items from it, you can do the following:

```python
from itertools import islice

first_five_items = list(islice(my_gen, 5))
```

# Section 2: Taking the First N Items from a List

To take the first N items from a list, you can use the built-in `list.slice` method. The `slice` method takes two arguments: a `start` index and a `stop` index. The `start` index specifies the index of the first item you want to take, and the `stop` index specifies the index of the item after the last item you want to take.

For example, if you have a list `my_list` and you want to take the first 5 items from it, you can do the following:

```python
first_five_items = my_list[:5]
```

# Section 3: Taking the Last N Items from a Generator

To take the last N items from a generator, you can use the `itertools.tee` and `itertools.islice` functions. The `tee` function takes a generator as its argument and returns two separate iterators for the same generator. The `islice` function takes a generator as its first argument, and the second argument is a `start` value that specifies the index of the item after the last item you want to take.

For example, if you have a generator `my_gen` and you want to take the last 5 items from it, you can do the following:

```python
from itertools import tee, islice

my_gen_1, my_gen_2 = tee(my_gen)

last_five_items = list(islice(my_gen_2, -5, None))
```

# Section 4: Taking the Last N Items from a List

To take the last N items from a list, you can use the built-in `list.slice` method. The `slice` method takes two arguments: a `start` index and a `stop` index. The `start` index specifies the index of the item after the last item you want to take, and the `stop` index is `None`.

For example, if you have a list `my_list` and you want to take the last 5 items from it, you can do the following:

```python
last_five_items = my_list[-5:]
```
