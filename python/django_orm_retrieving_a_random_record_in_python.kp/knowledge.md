---
title: What's the method to retrieve a random record using django's orm?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the .order\_by(`?`).first() method on your model queryset to pull a random record.
---

**Contents**

[TOC]

1. Set up the Django's ORM environment
Before using Django's ORM, the environment must be set up. To do this, import the necessary modules and set up the database by running the command `python manage.py migrate`.

2. Retrieve a random record from the database
To retrieve a random record, use the `order_by()` and `first()` methods in combination. The `order_by()` method is used to arrange the content of the database in a random order, and the `first()` method is used to select the first record in the resulting list.

```python
from myapp.models import MyModel
import random

# get the count of records in the table
count = MyModel.objects.count()
# retrieve a random object from the table
random_obj = MyModel.objects.order_by('?').first()
```

3. Display the random record
Once the random record is retrieved, it can be displayed in the desired format. For example, the attributes of the random record can be accessed using dot notation.

```python
print(random_obj.attribute1)
print(random_obj.attribute2)
```

4. Handle empty tables
If the table is empty, an error will occur when trying to retrieve a random record, so it is necessary to handle this exception case. One way to do this is to check the count of records in the database and only retrieve a random record if there is at least one record.

```python
from myapp.models import MyModel
import random

# get the count of records in the table
count = MyModel.objects.count()
# check if table is not empty
if count > 0:
   # retrieve a random object from the table
   random_obj = MyModel.objects.order_by('?').first()
else:
   print('Table is empty')
```
