---
title: Add numerous values to a single key in a dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A dictionary in Python can have multiple values for one key if each value is stored as a list, tuple or set.
---

**Contents**

[TOC]

1. Introduction
Dictionaries in Python allow us to map values to corresponding keys. In many cases, we may want to append multiple values to a single key in a dictionary. This can be done using various approaches in Python.

2. Using a list as a value for a dictionary key
One way to append multiple values to a single key in a dictionary is to define a list as a value for that key. As we know, lists can hold multiple values. To add more values to the list, we can use the append() method. Here's an example:

```
# define an empty dictionary
my_dict = {}

# add multiple values to a single key
my_dict['fruit'] = []
my_dict['fruit'].append('apple')
my_dict['fruit'].append('orange')
my_dict['fruit'].append('banana')

print(my_dict)
```

Output:
```
{'fruit': ['apple', 'orange', 'banana']}
```

In this example, we first define an empty dictionary. Then, we add a key called "fruit" and define its value as an empty list. Finally, we use the append() method to add three fruits to the list.

3. Using defaultdict from the collections module
Another way to append multiple values to a single key in a dictionary is to use defaultdict from the collections module. defaultdict is similar to a regular dictionary, but it automatically initializes any new key to a default value. In this case, we can set the default value to be an empty list. Here's an example:

```
from collections import defaultdict

# define a defaultdict with a default value of an empty list
my_dict = defaultdict(list)

# add multiple values to a single key
my_dict['fruit'].append('apple')
my_dict['fruit'].append('orange')
my_dict['fruit'].append('banana')

print(my_dict)
```

Output:
```
{'fruit': ['apple', 'orange', 'banana']}
```

In this example, we import defaultdict from the collections module and define it with a default value of an empty list. Then, we add the same fruits as in the previous example to the "fruit" key using the append() method.

4. Using setdefault() method
A third approach to append multiple values to a single key in a dictionary is to use the setdefault() method. This method sets the value of a key if it is not already in the dictionary. If the key is already in the dictionary, it returns the value of that key. Here's an example:

```
# define an empty dictionary
my_dict = {}

# add multiple values to a single key using setdefault()
my_dict.setdefault('fruit', []).append('apple')
my_dict.setdefault('fruit', []).extend(['orange', 'banana'])

print(my_dict)
```
Output:
```
{'fruit': ['apple', 'orange', 'banana']}
```

In this example, we first define an empty dictionary. Then, we use the setdefault() method to add the first fruit, 'apple', to the "fruit" key. In the second line, we use the setdefault() method again to add the list ['orange', 'banana'] to the "fruit" key using the extend() method. 

5. Conclusion
Appending multiple values to a single key in a dictionary can be achieved using multiple approaches in Python. We can use a list as a value for a dictionary key, use defaultdict from the collections module or use the setdefault() method. Depending on the specific use case, one of these approaches may be more suitable than the others.
