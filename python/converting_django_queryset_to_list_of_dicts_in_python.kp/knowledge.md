---
title: What is the process for converting a django queryset to a list of dictionaries?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the values() method on the QuerySet object to convert it into a list of dictionaries.
---

**Contents**

[TOC]

## Converting a Django QuerySet into a List of Dicts

Here's how you can convert a Django QuerySet into a list of dicts in Python:

### Step 1: Get the QuerySet

```python
queryset = MyModel.objects.all()
```

### Step 2: Convert the QuerySet to a list of dicts

```python
result_list = list(queryset.values())
```

This will convert the QuerySet to a list of dicts, where each dict represents a row in the database table.

### Additional Steps

If you want to include only certain fields in the dicts, you can specify them in the `values()` method. For example, if you want to include only the `name` and `age` fields:

```python
result_list = list(queryset.values('name', 'age'))
```

You can also add additional fields to each dict using dictionary comprehension:

```python
result_list = [{
    'name': item['name'],
    'age': item['age'],
    'fullname': '{} {}'.format(item['first_name'], item['last_name']),
} for item in queryset.values('name', 'age', 'first_name', 'last_name')]
```

This will include the `fullname` field in each dict, which is constructed from the `first_name` and `last_name` fields.
