---
title: In python, what is the process for combining two generators (or other iterables)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `itertools.chain` function to join two generators (or other iterables) in Python.
---

**Contents**

[TOC]

## Section 1: Using the `chain()` Function

The `chain()` function from `itertools` module can be used to join two generators (or other iterables) in Python. It takes two or more iterables and returns a single iterator that yields elements from each iterable in sequence.

Here's an example:

```python
from itertools import chain

gen1 = (x for x in range(1, 4))
gen2 = (x for x in range(4, 7))

gen = chain(gen1, gen2)

for i in gen:
    print(i)
```

Output:
```
1
2
3
4
5
6
```

In this example, we create two generator expressions `gen1` and `gen2`, which yield numbers 1 to 3 and 4 to 6 respectively. Then we pass both of these generators to the `chain()` function and create a new generator `gen`. Finally, we iterate over `gen` using a `for` loop to print all the elements.


## Section 2: Using the `+` Operator

In Python, the `+` operator can also be used to join two generators. To do this, we need to convert the generators into lists, concatenate them using the `+` operator, and then convert the resulting list back into a generator.

Here's an example:

```python
gen1 = (x for x in range(1, 4))
gen2 = (x for x in range(4, 7))

gen = (x for x in list(gen1) + list(gen2))

for i in gen:
    print(i)
```

Output:
```
1
2
3
4
5
6
```

In this example, we create two generator expressions `gen1` and `gen2`, which yield numbers 1 to 3 and 4 to 6 respectively. Then we convert both of these generators into lists, concatenate the lists using the `+` operator, and create a new generator by passing the concatenated list to a new generator expression. Finally, we iterate over the new generator using a `for` loop to print all the elements.


## Section 3: Using the `zip()` Function

We can also join two generators by using the `zip()` function. The `zip()` function takes two or more iterables and returns an iterator that yields tuples containing the corresponding elements from each iterable.

Here's an example:

```python
gen1 = (x for x in range(1, 4))
gen2 = (x for x in range(4, 7))

gen = (x for pair in zip(gen1, gen2) for x in pair)

for i in gen:
    print(i)
```

Output:
```
1
4
2
5
3
6
```

In this example, we create two generator expressions `gen1` and `gen2`, which yield numbers 1 to 3 and 4 to 6 respectively. Then we passing both of these generators to the `zip()` function to get an iterator that yields pairs of corresponding elements from both generators. Finally, we create a new generator that iterates over the pairs and yields each element from each pair in sequence. We then iterate over this new generator using a `for` loop to print all the elements.


## Section 4: Combining Generators Using `yield from` (Python 3.3+)

In Python 3.3 and above, the most elegant way to join two or more generators is to use the `yield from` statement. The `yield from` statement can be used to delegate the task of iterating over one or more iterators to another iterator.

Here's an example:

```python
def combined_gen(gen1, gen2):
    yield from gen1
    yield from gen2

gen1 = (x for x in range(1, 4))
gen2 = (x for x in range(4, 7))

gen = combined_gen(gen1, gen2)

for i in gen:
    print(i)
```

Output:
```
1
2
3
4
5
6
```

In this example, we define a new generator function `combined_gen()` that takes two generators as arguments and uses the `yield from` statement to delegate the task of iterating over each generator to the `gen` generator. We then create two generator expressions `gen1` and `gen2`, which yield numbers 1 to 3 and 4 to 6 respectively. Finally, we pass both of these generators to the `combined_gen()` function and create a new generator `gen`. We then iterate over `gen` using a `for` loop to print all the elements.
