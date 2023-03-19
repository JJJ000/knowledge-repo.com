---
title: How can I sort one list and rearrange the other in parallel when both lists are parallel?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can use the built-in zip function and the sorted function to sort one list while permuting the other in the same way.
---

**Contents**

[TOC]

# Step 1: Create two parallel lists

The first step is to create two parallel lists that need to be sorted and permuted accordingly.


```python
names = ['Alice', 'Bob', 'Charlie', 'David']
scores = [70, 80, 60, 90]
```


# Step 2: Combine the lists

Next, we can combine the lists into a single list of tuples using the `zip` function. 


```python
combined = list(zip(scores, names))
print(combined)
```

    [(70, 'Alice'), (80, 'Bob'), (60, 'Charlie'), (90, 'David')]



# Step 3: Sort the combined list

We can then sort the combined list based on the first element of each tuple (the scores). 


```python
combined.sort(reverse=True)
print(combined)
```

    [(90, 'David'), (80, 'Bob'), (70, 'Alice'), (60, 'Charlie')]



# Step 4: Separate the lists

Finally, we can separate the sorted list of tuples back into two parallel lists.


```python
scores, names = zip(*combined)
print(scores)
print(names)
```

    (90, 80, 70, 60)
    ('David', 'Bob', 'Alice', 'Charlie')


The above code sorts the scores in decreasing order and permutes the names list accordingly.
