---
title: How can you import YAML mappings as ordereddicts using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the `yaml.load()` function from the PyYAML library with the `Loader=yaml.FullLoader` parameter to load YAML mappings as OrderedDicts.
---

**Contents**

[TOC]

## Introduction

YAML is a human-readable data serialization format that is commonly used in configurations, data exchange, and application states. Python provides a built-in `yaml` module that can be used to load and dump YAML data with ease. 

When loading YAML mappings, it can be useful to preserve the order in which the keys appear. The `yaml` module provides an option to load mappings as `OrderedDicts`, which are data structures that preserve the order in which items are added. This can be helpful when working with YAML data that requires a specific order of keys.

In this tutorial, we'll go through the steps of loading YAML mappings as `OrderedDicts` in Python.

## Step 1: Install the PyYAML package

The `yaml` module is part of the Python standard library, which means it comes pre-installed with Python. However, to load YAML mappings as `OrderedDicts`, we need to use the `ruamel.yaml` package, which is a more advanced YAML parser. The `ruamel.yaml` package is a superset of the `PyYAML` package, which means it can handle all the features of `PyYAML` while also providing additional functionality.

To install the `ruamel.yaml` package, you can use the following command:

```
pip install ruamel.yaml
```

## Step 2: Load YAML data as `OrderedDicts`

To load YAML data as `OrderedDicts`, we need to use the `ruamel.yaml` package instead of the built-in `yaml` module. Here's an example code snippet that demonstrates how to load a YAML file as an `OrderedDict`:

```python
import ruamel.yaml
from collections import OrderedDict

# Load a YAML file as an OrderedDict
with open('example.yaml', 'r') as f:
    data = ruamel.yaml.load(f, Loader=ruamel.yaml.Loader)
    data = OrderedDict(data)
```

In this example, we first import the `ruamel.yaml` package and the `OrderedDict` class from the built-in `collections` module. We then use the `with` statement to open a YAML file (`example.yaml`) in read mode. 

We load the YAML data using the `ruamel.yaml.load` function and pass in the `Loader` argument as `ruamel.yaml.Loader`. This tells the function to load the YAML data as an `OrderedDict`.

Finally, we convert the resulting `dict` into an `OrderedDict` using the `collections.OrderedDict` constructor.

## Step 3: Accessing the `OrderedDict`

Once we've loaded the YAML data as an `OrderedDict`, we can access the items in the same way as a regular `dict`. Here's an example:

```python
# Print the values in the loaded YAML file
for key, value in data.items():
    print(key, value)
```

In this example, we loop through the items in the `OrderedDict` using the `items` method. We then print out the key and value for each item.

## Conclusion

In this tutorial, we've gone through the steps of loading YAML mappings as `OrderedDicts` in Python. We've covered how to install the `ruamel.yaml` package, how to load YAML data as an `OrderedDict`, and how to access the items in the loaded `OrderedDict`. By following these steps, you can work with YAML data that requires a specific order of keys while still being able to use Python's `dict` data type.
