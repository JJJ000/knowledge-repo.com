---
title: Discover the initial element in a sequence that fulfills a predicate
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: The function `next()` with a generator expression can be used to find the first element in a sequence that matches a predicate in Python.
---

**Contents**

[TOC]

## Problem Statement

Given a sequence, we want to find the first element in the sequence that matches a given predicate. The sequence could be any iterable object, such as a list, tuple, or generator. The predicate is a function that returns a boolean value, indicating whether a given element matches a certain condition. 

## Solution

We can solve this problem using the `next()` function in Python. The `next()` function takes an iterable object and returns the next element in the sequence. We can use a loop to iterate over the sequence and call the predicate function for each element. If the predicate function returns True, we stop the loop and return the element. If no element matches the predicate, we raise a StopIteration exception. 

```python
def find_first(seq, predicate):
    """
    Find the first element in the sequence that matches a given predicate.

    Args:
      seq: Iterable object to search for the element
      predicate: Function that takes an element and returns a boolean value
      
    Returns:
      The first element in the sequence that matches the predicate
      
    Raises:
      StopIteration: If no element matches the predicate
    """
    for x in seq:
        if predicate(x):
            return x
    raise StopIteration
```

To use this function, we can define a predicate function and call `find_first()` with the sequence and predicate:

```python
seq = [1, 2, 3, 4, 5]
predicate = lambda x: x > 3
result = find_first(seq, predicate)
print(result) # Output: 4
```

In this example, the predicate function `lambda x: x > 3` checks whether the element is greater than 3. The `find_first()` function returns the first element in the sequence that satisfies this condition, which is 4.

## Example

Let's see another example where we find the first word in a list that starts with a certain character. 

```python
def find_first_word(words, letter):
    """
    Find the first word in a list that starts with a given letter.

    Args:
      words: List of words to search for the element
      letter: String representing the first letter of the word
      
    Returns:
      The first word in the list that starts with the given letter
      
    Raises:
      StopIteration: If no element matches the predicate
    """
    predicate = lambda word: word.startswith(letter)
    return find_first(words, predicate)
```

To use this function, we can define a list of words and call `find_first_word()` with the list and first letter:

```python
words = ["apple", "banana", "peach", "apricot"]
letter = "a"
result = find_first_word(words, letter)
print(result) # Output: "apple"
```

In this example, the `find_first_word()` function finds the first word in the list `words` that starts with the letter "a". The predicate function checks whether the word starts with this letter using the `startswith()` method. The function returns the first word in the list that matches the predicate, which is "apple".
