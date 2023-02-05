---
title: What is the process of creating a copy of a django model instance and saving it to the database?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Create a new instance of the model with the same values as the original instance, then call the new instance`s .save() method.
---

**Contents**

[TOC]

# Section 1: Import Necessary Modules

In order to clone a Django model instance object and save it to the database in Python, we need to import the following modules:

```
from django.db import models
from copy import deepcopy
```

# Section 2: Clone the Model Instance

We can use the `deepcopy` method from the `copy` module to clone the model instance. This will create a new instance of the model with the same values as the original instance.

```
original_instance = Model.objects.get(pk=1)
clone_instance = deepcopy(original_instance)
```

# Section 3: Set the Primary Key

Since the cloned instance is a new instance, it will have a different primary key (`pk`) than the original instance. We need to set the primary key of the cloned instance to `None` to indicate that it is a new instance.

```
clone_instance.pk = None
```

# Section 4: Save the Cloned Instance

Once the primary key has been set, we can save the cloned instance to the database.

```
clone_instance.save()
```
