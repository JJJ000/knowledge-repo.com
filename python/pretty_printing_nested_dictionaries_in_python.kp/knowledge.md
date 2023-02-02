---
title: What is the best way to format nested dictionaries for readability?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the `pprint` module to pretty print nested dictionaries in Python.
---

**Contents**

[TOC]

## Using the pprint Module

The [pprint](https://docs.python.org/3/library/pprint.html) module provides a `pprint()` function that is capable of pretty-printing nested dictionaries.

To use the `pprint()` function, first import the `pprint` module:

```python
import pprint
```

Then, call the `pprint()` function on the nested dictionary, passing the dictionary as an argument.

```python
pprint.pprint(nested_dict)
```

## Using the json Module

The [json](https://docs.python.org/3/library/json.html) module provides a `dumps()` function that can be used to pretty-print nested dictionaries.

To use the `dumps()` function, first import the `json` module:

```python
import json
```

Then, call the `dumps()` function on the nested dictionary, passing the dictionary as an argument.

```python
json.dumps(nested_dict, indent=4)
```

The `indent` argument specifies the number of spaces to indent for each level of nesting.

## Using the PrettyPrinter Class

The [pprint](https://docs.python.org/3/library/pprint.html) module provides a `PrettyPrinter` class that can be used to pretty-print nested dictionaries.

To use the `PrettyPrinter` class, first import the `pprint` module:

```python
import pprint
```

Then, create an instance of the `PrettyPrinter` class, and call its `pprint()` method on the nested dictionary, passing the dictionary as an argument.

```python
pp = pprint.PrettyPrinter(indent=4)
pp.pprint(nested_dict)
```

The `indent` argument specifies the number of spaces to indent for each level of nesting.
