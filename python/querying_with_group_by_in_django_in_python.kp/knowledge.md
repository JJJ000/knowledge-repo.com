---
title: What is the syntax for using group by in a django queryset?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: In Django, you can use the QuerySet.values() and QuerySet.annotate() methods to group query results by a given field.
---

**Contents**

[TOC]

1. **Importing the Necessary Modules** 

First, import the necessary modules from Django:

```python
from django.db import models
```

2. **Creating the Model** 

Next, create the model for the data you want to query:

```python
class MyModel(models.Model):
    name = models.CharField(max_length=50)
    age = models.IntegerField()
```

3. **Querying with GROUP BY** 

Finally, use the `.annotate()` method to query with `GROUP BY`:

```python
MyModel.objects.values('name').annotate(total_age=Sum('age'))
```

This will query the `MyModel` model and return the total age of each name.
