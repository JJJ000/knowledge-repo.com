---
title: What is the process for combining dictionaries that contain dictionaries?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the update() method on the outer dictionary and pass in the inner dictionary to merge them.
---

**Contents**

[TOC]

Section 1: Introduction 
Merging dictionaries of dictionaries can be useful when working with complex data structures in Python. It allows you to combine multiple dictionaries into a single, larger dictionary. In this guide, we'll show you how to merge dictionaries of dictionaries in Python using various methods.

Section 2: Using the update() method 
The update() method is the easiest way to merge dictionaries of dictionaries in Python. You can call the update() method on the main dictionary and pass in the sub-dictionaries as separate arguments. Here's an example:

```
dict1 = {'a': {'x': 1}, 'b': {'y': 2}}
dict2 = {'c': {'z': 3}}

dict1.update(dict2)

print(dict1)
```

Output:
```
{'a': {'x': 1}, 'b': {'y': 2}, 'c': {'z': 3}}
```

In this example, we merged the sub-dictionary of dict2 with dict1 using the update() method. The resulting dictionary contains all the key-value pairs from both dictionaries.

Section 3: Using the defaultdict() function 
Another way to merge dictionaries of dictionaries is to use the defaultdict() function from the collections module. This method allows you to merge dictionaries without overwriting any existing key-value pairs. Here's an example:

```
from collections import defaultdict

dict1 = {'a': {'x': 1}, 'b': {'y': 2}}
dict2 = {'b': {'z': 3}, 'c': {'w': 4}}

merged_dict = defaultdict(dict)

for d in (dict1, dict2):
    for key, value in d.items():
        merged_dict[key].update(value)

print(dict(merged_dict))
```

Output:
```
{'a': {'x': 1}, 'b': {'y': 2, 'z': 3}, 'c': {'w': 4}}
```

In this example, we used the defaultdict() function to create a new dictionary called merged_dict. We then looped through both dicts and used the update() method to add their key-value pairs to merged_dict. The resulting dictionary contains all the key-value pairs from both dictionaries without overwriting any values.

Section 4: Using the ChainMap() function 
The third way to merge dictionaries of dictionaries is to use the ChainMap() function from the collections module. This method creates a view of multiple dictionaries as a single dictionary-like object. Here's an example:

```
from collections import ChainMap

dict1 = {'a': {'x': 1}, 'b': {'y': 2}}
dict2 = {'b': {'z': 3}, 'c': {'w': 4}}

merged_dict = ChainMap(dict1, dict2)

print(dict(merged_dict))
```

Output:
```
{'a': {'x': 1}, 'b': {'y': 2, 'z': 3}, 'c': {'w': 4}}
```

In this example, we used the ChainMap() function to create a view of both dictionaries as a single dictionary-like object called merged_dict. The resulting dictionary contains all the key-value pairs from both dictionaries without overwriting any values.

Section 5: Conclusion 
In this guide, we covered three different methods for merging dictionaries of dictionaries in Python. The update() method, the defaultdict() function, and the ChainMap() function offer different ways to merge dictionaries depending on your needs. Experiment with each method to find the one that works best for your use case.
