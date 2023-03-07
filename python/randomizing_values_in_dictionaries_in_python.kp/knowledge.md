---
title: What is the method to obtain a random value from a dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the random module`s choice() method with the dictionary`s key or value as the argument to get a random value from a dictionary in Python.
---

**Contents**

[TOC]

### Creating a dictionary in Python

Before we can retrieve a random value from a dictionary, we first need to create a dictionary. A dictionary in Python is created using braces `{}` and key-value pairs separated by colons `:`. Here is an example of a dictionary of programming languages and their years of initial release:

``` python
programming_languages = {
    'Python': 1991,
    'Java': 1995,
    'JavaScript': 1995,
    'C++': 1983,
    'Ruby': 1995
}
```

### Getting a random key from a dictionary

To get a random key from a dictionary, we can use the `random` module in Python. The `random.choice()` method can be used to pick a random element from a list. However, since a dictionary is not a list, we need to first convert the keys of the dictionary into a list using the `list()` function. Here is an example:

``` python
import random

programming_languages = {
    'Python': 1991,
    'Java': 1995,
    'JavaScript': 1995,
    'C++': 1983,
    'Ruby': 1995
}

random_key = random.choice(list(programming_languages.keys()))

print(random_key)
```

The `keys()` method returns a view object of the dictionary keys, which we convert into a list using the `list()` function. Then, we use `random.choice()` to pick a random key from the list of keys, which is stored in the `random_key` variable. Finally, we print the random key.

### Getting a random value from a dictionary

To get a random value from a dictionary, we can modify the previous code slightly to retrieve the value stored under the randomly chosen key. Here is an example:

``` python
import random

programming_languages = {
    'Python': 1991,
    'Java': 1995,
    'JavaScript': 1995,
    'C++': 1983,
    'Ruby': 1995
}

random_key = random.choice(list(programming_languages.keys()))
random_value = programming_languages[random_key]

print(random_value)
```

In this example, after we randomly choose a key in the same way as before (`random.choice(list(programming_languages.keys()))`), we retrieve the value associated with the key using bracket notation on the dictionary (`programming_languages[random_key]`). This value is stored in the `random_value` variable, which we then print.

### Getting a random key-value pair from a dictionary

If we want to retrieve a random key-value pair from a dictionary, we can combine the methods shown above. Here is an example:

``` python
import random

programming_languages = {
    'Python': 1991,
    'Java': 1995,
    'JavaScript': 1995,
    'C++': 1983,
    'Ruby': 1995
}

random_key = random.choice(list(programming_languages.keys()))
random_value = programming_languages[random_key]

random_pair = {random_key: random_value}

print(random_pair)
```

In this example, we first randomly choose a key from the dictionary with `random.choice(list(programming_languages.keys()))`. We then retrieve the value for the random key with `programming_languages[random_key]`. Finally, we create a new dictionary containing the random key-value pair with `{random_key: random_value}` and store it in the `random_pair` variable. We then print the random key-value pair.
