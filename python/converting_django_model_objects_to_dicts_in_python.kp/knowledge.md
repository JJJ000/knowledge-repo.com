---
title: Transform a django model object into a dictionary containing all its fields
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the model\_to\_dict() method from the Django Model class to convert a Django Model object to a dict with all of its fields intact.
---

**Contents**

[TOC]

### Section 1: Using Django's Model_to_dict() Method

Django provides a built-in method called `model_to_dict()` which can be used to convert a Django Model object to a dictionary.

The syntax for using this method is as follows:

```python
model_to_dict(instance, fields=None, exclude=None)
```

Where `instance` is the Django Model object to be converted, `fields` is an optional list of field names to include in the dictionary, and `exclude` is an optional list of field names to exclude from the dictionary.

The method will return a dictionary containing all of the fields from the Model object, or a subset of fields if the `fields` or `exclude` parameters are used.

### Section 2: Using Django's Values() Method

Django also provides a built-in method called `values()` which can be used to convert a Django Model object to a dictionary.

The syntax for using this method is as follows:

```python
values(fields=None, exclude=None)
```

Where `fields` is an optional list of field names to include in the dictionary, and `exclude` is an optional list of field names to exclude from the dictionary.

The method will return a dictionary containing all of the fields from the Model object, or a subset of fields if the `fields` or `exclude` parameters are used.

### Section 3: Using Python's vars() Method

Python also provides a built-in method called `vars()` which can be used to convert a Django Model object to a dictionary.

The syntax for using this method is as follows:

```python
vars(instance)
```

Where `instance` is the Django Model object to be converted.

The method will return a dictionary containing all of the fields from the Model object.

### Section 4: Using Python's dict() Method

Python also provides a built-in method called `dict()` which can be used to convert a Django Model object to a dictionary.

The syntax for using this method is as follows:

```python
dict(instance)
```

Where `instance` is the Django Model object to be converted.

The method will return a dictionary containing all of the fields from the Model object.
