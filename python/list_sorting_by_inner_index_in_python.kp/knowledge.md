---
title: What is the method for arranging a list of lists according to a specific index within the inner list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the sorted() function with a lambda function as the key parameter to sort by a specific index of the inner list.
---

**Contents**

[TOC]

### Section 1: Creating a List of Lists

To demonstrate how to sort a list of lists by a specific index of the inner list in Python, we first need to create a list of lists. In this example, we will create a list of lists containing information about different countries: the name of the country, the population, and the GDP per capita. Each inner list will contain this information as strings.

```python
countries = [
    ['United States', '328.2 million', '$59,501'],
    ['China', '1.4 billion', '$10,261'],
    ['Germany', '83.1 million', '$52,556'],
    ['United Kingdom', '66.0 million', '$42,330'],
    ['India', '1.3 billion', '$2,104']
]
```

### Section 2: Sorting the List of Lists by Index

To sort the list of lists by a specific index, we can use Python's built-in `sorted` function and pass in a lambda function as the `key` argument. The lambda function will return the value of the index we want to sort by for each inner list.

For example, to sort the list of lists by the GDP per capita (which is at index 2 of each inner list), we can use the following code:

```python
sorted_countries = sorted(countries, key=lambda x: x[2])
```

This will return a new sorted list of lists based on the GDP per capita:

```
[['India', '1.3 billion', '$2,104'],
 ['China', '1.4 billion', '$10,261'],
 ['United Kingdom', '66.0 million', '$42,330'],
 ['United States', '328.2 million', '$59,501'],
 ['Germany', '83.1 million', '$52,556']]
```


### Section 3: Reversing the Sort Order

To reverse the sort order (e.g., from ascending to descending), we can simply add the `reverse=True` argument to the `sorted` function.

For example, to sort the list of lists by GDP per capita in descending order, we can use the following code:

```python
sorted_countries_desc = sorted(countries, key=lambda x: x[2], reverse=True)
```

This will return a new sorted list of lists based on GDP per capita in descending order:

```
[['Germany', '83.1 million', '$52,556'],
 ['United States', '328.2 million', '$59,501'],
 ['United Kingdom', '66.0 million', '$42,330'],
 ['China', '1.4 billion', '$10,261'],
 ['India', '1.3 billion', '$2,104']]
```


### Section 4: Modifying the Inner List Based on the Sorted Order

If we want to modify the inner list based on the sorted order, we can use a for loop and the `enumerate` function to iterate over the sorted list of lists and update each inner list with a new value, such as a rank.

For example, to add a rank to each inner list based on the sorted order by GDP per capita, we can use the following code:

```python
for i, country in enumerate(sorted_countries_desc):
    rank = i + 1
    country.append(rank)

print(sorted_countries_desc)
```

This will output:

```
[['Germany', '83.1 million', '$52,556', 1],
 ['United States', '328.2 million', '$59,501', 2],
 ['United Kingdom', '66.0 million', '$42,330', 3],
 ['China', '1.4 billion', '$10,261', 4],
 ['India', '1.3 billion', '$2,104', 5]]
```

Now, each inner list has a new value at the end representing its rank based on the sorted order by GDP per capita.
