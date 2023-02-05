---
title: How should one properly use Python argparse.namespace() as if it were a dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The best way to treat a Python argparse.Namespace() as a dictionary is to use the vars() method.
---

**Contents**

[TOC]

1. Accessing Arguments as Dictionary Keys 

The `vars()` function can be used to convert the `Namespace` object to a dictionary. This function returns a dictionary containing the namespace object's attribute names as keys and their corresponding values as values.

Example:

```
my_namespace = argparse.Namespace(name='John', age=30)
my_dict = vars(my_namespace) 
print(my_dict)
# {'name': 'John', 'age': 30}
```

2. Updating Arguments in the Dictionary 

The `update()` method can be used to update the `Namespace` object with values from a dictionary. This method adds the items from the dictionary to the `Namespace` object.

Example:

```
my_namespace = argparse.Namespace(name='John', age=30)
my_dict = {'name': 'Jane', 'height': 5.5}
my_namespace.update(my_dict)
print(vars(my_namespace))
# {'name': 'Jane', 'age': 30, 'height': 5.5}
```

3. Adding New Arguments to the Dictionary 

The `setattr()` method can be used to add new arguments to the `Namespace` object. This method takes two arguments: the attribute name and the value to be set.

Example:

```
my_namespace = argparse.Namespace(name='John', age=30)
setattr(my_namespace, 'height', 5.5)
print(vars(my_namespace))
# {'name': 'John', 'age': 30, 'height': 5.5}
```

4. Deleting Arguments from the Dictionary 

The `delattr()` method can be used to delete arguments from the `Namespace` object. This method takes one argument: the attribute name to be deleted.

Example:

```
my_namespace = argparse.Namespace(name='John', age=30, height=5.5)
delattr(my_namespace, 'height')
print(vars(my_namespace))
# {'name': 'John', 'age': 30}
```
