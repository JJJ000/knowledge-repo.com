---
title: Verify if there are any words from a list present in a separate string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `in` keyword to check if a string contains a specific set of words.
---

**Contents**

[TOC]

# Approach

- The problem statement requires us to check if a list of words exist in a given string, and if yes we should return `True`, else `False`.
- We can solve this problem by iterating through the list of words and checking if each word exists in the given string.
- There are multiple ways to check if a word exists in a string, we will explore a few of them in the following sections.
- Our approach will be to create a function that takes in two parameters - the string and the list of words, and returns `True` or `False` based on whether all the words exist in the string or not.


## Using the `in` operator

- One of the simplest ways to check if a word exists in a string is to use the `in` operator.
- We can loop through the list of words and check if each word is present in the string using the `in` operator.
- If any word is not found in the string, we can immediately return `False`, else we can return `True`.
- Below is the code implementation for this approach.

```python
def check_words_in_string(string, word_list):
    for word in word_list:
        if word not in string:
            return False
    return True
```


## Using regular expressions

- Regular expressions are a powerful tool for pattern matching and searching in strings.
- We can use regular expressions to search for a pattern that matches any of the words in the list.
- The regular expression would look something like `word1|word2|word3`, where `word1`, `word2` and `word3` are the words in the list.
- We can then use the `re.search()` function to search for this pattern in the given string.
- If a match is found, the function would return a match object which is truthy, else it would return `None` which is falsy.
- Below is the code implementation for this approach.

```python
import re

def check_words_in_string(string, word_list):
    regex_pattern = '|'.join(word_list)
    match_object = re.search(regex_pattern, string)
    
    if match_object:
        return True
    else:
        return False
```


## Using set intersection

- Another approach is to convert the string and the list of words to sets and then take the intersection of the two sets.
- We can then check if the intersection set is equal to the set of all the words in the list.
- If it is, then all the words exist in the string, else they don't.
- Below is the code implementation for this approach.

```python
def check_words_in_string(string, word_list):
    string_set = set(string.split())
    word_set = set(word_list)
    
    if word_set.intersection(string_set) == word_set:
        return True
    else:
        return False
```


# Conclusion

- In this problem, we looked at different approaches to check if a list of words exist in a given string.
- We explored the `in` operator, regular expressions and set intersection.
- All of these approaches are valid and produce the correct output.
- Depending on the requirements and constraints of the problem, we can use any of these approaches to solve this problem.
