---
title: How can an option without an argument be included in the argparse module?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To add an option without any argument in argparse module, use the action=`store\_true` parameter in the add\_argument() method.
---

**Contents**

[TOC]

### Introduction to argparse module

The `argparse` module in Python provides a simple and user-friendly way to parse command-line arguments. It is used to write user-friendly command-line interfaces.

The following sections will demonstrate how to add an option without any argument in Python using the `argparse` module.


### Step 1: Import the argparse module

To use the `argparse` module, we first need to import it. The following code demonstrates how to import the `argparse` module:

```python
import argparse
```


### Step 2: Create an ArgumentParser object

The `ArgumentParser` class in the `argparse` module is used to define the command-line interface. We can create an instance of the `ArgumentParser` class using the following code:

```python
parser = argparse.ArgumentParser()
```

### Step 3: Adding an option without any argument

We can add an option without any argument using the `add_argument()` method of the `ArgumentParser` class. We just need to set the `action` parameter to `'store_true'`. This will create an option that does not require any argument.

```python
parser.add_argument('--option', help='This is an option', action='store_true')
```

The above code will add an option called `--option` to the command-line interface. When this option is specified, the `option` variable will be set to `True`.

### Step 4: Parsing the arguments

After we have defined the command-line interface using the `ArgumentParser` class, we need to parse the arguments using the `parse_args()` method. The following code demonstrates how to parse the arguments:

```python
args = parser.parse_args()
```

This will parse the command-line arguments and store the values in the `args` variable.

### Conclusion

In this tutorial, we have learned how to add an option without any argument using the `argparse` module in Python. We first imported the `argparse` module and created an instance of the `ArgumentParser` class. Then, we added an option without any argument using the `add_argument()` method and parsed the arguments using the `parse_args()` method.
