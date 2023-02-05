---
title: Show a help message using Python argparse when the script is run without any arguments
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The argparse module can be used to display a help message when the script is called without any arguments by using the add\_argument method with the action=`help` argument.
---

**Contents**

[TOC]

### Using the `add_help` Argument

The `add_help` argument is a boolean parameter that is set to `True` by default. When `add_help` is set to `True`, argparse will automatically add a `-h` or `--help` argument that will print a help message when the script is called without any arguments.

### Writing the Help Message

The help message should provide a brief overview of the script and its arguments. It should include the name of the script, a short description, and a list of arguments with a description of each argument.

### Adding the `--help` Argument

The `--help` argument can be added to the script by creating a parser object and setting the `add_help` parameter to `True`. For example:

```python
parser = argparse.ArgumentParser(description='My Script', add_help=True)
```

### Printing the Help Message

The help message can be printed by calling the `print_help` method on the parser object. For example:

```python
parser.print_help()
```
