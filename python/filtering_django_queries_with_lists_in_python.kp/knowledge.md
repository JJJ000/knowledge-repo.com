---
title: What is the best way to use a list of values to limit the results of a django query?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the `\_\_in` lookup to filter the query with a list of values.
---

**Contents**

[TOC]

**Using the `__in` Lookup**

The `__in` lookup can be used to filter a Django query with a list of values. This lookup allows you to specify a list of values and will return all objects that match any of those values.

**Syntax**

The syntax for using the `__in` lookup is as follows:

```
Model.objects.filter(field_name__in=[list_of_values])
```

**Example**

For example, if you wanted to filter a query for all objects with a `color` field that is either `red` or `blue`, you could use the following syntax:

```
Model.objects.filter(color__in=['red', 'blue'])
```

**Limitations**

The `__in` lookup can only be used with fields that are stored in the database. It cannot be used with computed fields or fields with custom lookup types.
