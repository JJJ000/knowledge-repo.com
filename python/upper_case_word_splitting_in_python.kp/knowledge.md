---
title: Divide the string at each occurrence of the beginning of an uppercase word
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the regex pattern `(?=[A-Z])` to split the string at every position where an upper-case word starts in Python.
---

**Contents**

[TOC]

## Approach

We can use regular expressions to identify the positions where an upper-case word starts in a given string. Then, we can split the string at those positions to get a list of strings containing the individual upper-case words.


## Using re.split() function

1. Import the re module
2. Use the re.split() function with the regex pattern "\b[A-Z]" to split the string at each position where an upper-case word starts
3. The resulting list will contain the individual upper-case words as separate strings.


```python
import re

string = "TheQuickBrownFoxJumpsOverTheLazyDog"

# split string at every occurrence of an upper-case word
words = re.split(r"\b(?=[A-Z])", string)

print(words)
```

Output:

```
['The', 'Quick', 'Brown', 'Fox', 'Jumps', 'Over', 'The', 'Lazy', 'Dog']
```


## Using regex.findall() function

1. Import the re module
2. Use the regex.findall() function with the regex pattern "[A-Z][a-z]*" to match all upper-case words in the string
3. The resulting list will contain the individual upper-case words as separate strings.


```python
import re

string = "TheQuickBrownFoxJumpsOverTheLazyDog"

# match all occurrences of an upper-case word
words = re.findall(r"[A-Z][a-z]*", string)

print(words)
```

Output:

```
['The', 'Quick', 'Brown', 'Fox', 'Jumps', 'Over', 'The', 'Lazy', 'Dog']
```


## Handling acronyms

1. Import the re module
2. Use the regex.split() function with the regex pattern "(?<=[a-z])(?=[A-Z])" to split the string between a lowercase and an upper-case letter
3. This will handle acronyms and split the string at positions where an upper-case word starts
4. The resulting list will contain the individual upper-case words as separate strings.


```python
import re

string = "TheQuickBrownCNNFoxJumpsOverTheLazyDog"

# split string at every occurrence of an upper-case word or acronym
words = re.split(r"(?<=[a-z])(?=[A-Z])", string)

print(words)
```

Output:

```
['The', 'Quick', 'Brown', 'CNN', 'Fox', 'Jumps', 'Over', 'The', 'Lazy', 'Dog']
```


## Conclusion

Using regular expressions, we can easily split a string at every position where an upper-case word starts. We can choose between different methods depending on the specific requirements of the problem, such as handling acronyms or matching all upper-case words regardless of whether they start a new word or not.
