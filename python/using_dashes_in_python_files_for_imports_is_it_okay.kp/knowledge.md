---
title: Can dashes be used in Python files for importing purposes without any issues?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Yes, it is okay to use dashes in Python file names, however, when importing them, you must replace the dash with an underscore.
---

**Contents**

[TOC]

Yes, it is OK to use dashes in Python file names when trying to import them. Here are some reasons why:

## Valid file name characters

According to the Python documentation, there are only a few restrictions on file name characters. In particular, a file name can include letters, digits, and underscores. However, the documentation also states that "it is best to only use ASCII characters in file names." Dashes are ASCII characters, so there is no reason why they cannot be used in file names.

## Convention for module naming

In Python, it is common practice to use underscores in module names to separate words, rather than dashes. For example, if you have a module that provides functionality for working with dates and times, you might call it "datetime_utils.py". This convention is not a strict requirement, but it does help make module names more readable.

## Importing conventions

When you import a Python module, you typically use the module name without any file extension or path information. For example, if you have a module called "my_module.py" in the same directory as your script, you can import it like this:

```python
import my_module
```

If you have a module with a dash in its name, such as "my-module.py", you can still import it using the same syntax:

```python
import my_module
```

In this case, Python will look for a file called "my_module.py" or "my_module/__init__.py" in the same directory as the script.

## Conclusion

In summary, using dashes in Python file names is generally acceptable, as long as the other characters in the file name are valid and the file is imported using the appropriate syntax. However, it is best to follow Python's recommended convention of using underscores in module names for better readability.
