---
title: How to retrieve a value from a dictionary using a variable in a django template
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To look up a dictionary value with a variable in Django templates, use the `dot` notation to access the dictionary value with the variable as the key.
---

**Contents**

[TOC]

1. Introduction
In Django template, it is common to use dictionaries to store values associated with keys, but sometimes we need to look up a dictionary value with a variable instead of a hardcoded key. In this article, we will explore how to do it in Python.

2. Using dictionary.get() method
The easiest way to look up a dictionary value with a variable is to use the dictionary.get() method. This method takes a key as the first parameter and a default value as the second parameter (optional). If the key is not found in the dictionary, the default value will be returned. Here is an example:

```
my_dict = {'a': 1, 'b': 2, 'c': 3}
my_key = 'b'
my_value = my_dict.get(my_key, 0)
```

In this example, we have a dictionary called my_dict with three key-value pairs. We also have a variable my_key set to 'b', which is the key we want to look up. Finally, we use the dictionary.get() method to retrieve the value of 'b' from my_dict. If 'b' is not found in my_dict, the default value of 0 will be returned.

3. Using dictionary indexing
Another way to look up dictionary values with a variable is to use dictionary indexing. This requires us to use the square bracket notation to access the dictionary, like this:

```
my_dict = {'a': 1, 'b': 2, 'c': 3}
my_key = 'b'
my_value = my_dict[my_key]
```

In this example, we are doing the same thing as before, but using dictionary indexing instead. We access the value of 'b' by using my_dict[my_key], where my_key is the variable holding the key we want to look up.

However, please note that this method can throw a KeyError if the key does not exist in the dictionary. Therefore, it is safer to use the first method (dictionary.get()) if there is any doubt about whether the key exists.

4. Conclusion
In conclusion, we have explored two ways to look up dictionary values with a variable in Python. The first method, dictionary.get(), allows us to provide a default value in case the key does not exist. The second method, dictionary indexing, is simpler but can throw a KeyError if the key does not exist. Hopefully, this article has been helpful in understanding how to look up dictionary values with a variable in Django template.
