---
title: What is the way to apply a filter to a particular date in a datetimefield in django?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To filter by a specific date, use the `.filter()` method with the date object as the argument, like this `ExampleModel.objects.filter(datetime\_field\_\_date=date\_object)`.
---

**Contents**

[TOC]

## Section 1 - Introduction
In Django, the `DateTimeField` is often used to store dates and times. For example, it might be used to store the date that an event occurred or the time that a message was sent. When working with `DateTimeField` fields, it can sometimes be necessary to filter the results based on a specific date. This tutorial will show you how to filter a date of a `DateTimeField` in Django using Python.

## Section 2 - Filter by specific date
To filter a `DateTimeField` by a specific date, you can use the `__date` lookup. This will filter the results to include only those where the date of the `DateTimeField` matches the specified date. Here is an example:

```python
from datetime import date
from myapp.models import MyModel

my_date = date(2022, 2, 22)
results = MyModel.objects.filter(my_date_field__date=my_date)
```

In this example, we are filtering the `MyModel` model by the `my_date_field` field, which is a `DateTimeField`. We are using the `__date` lookup to filter the results to include only those where the date of the field matches `my_date`.

## Section 3 - Filter by range of dates
To filter a `DateTimeField` by a range of dates, you can use the `__gte` (greater than or equal to) and `__lte` (less than or equal to) lookups. These will filter the results to include only those where the date of the `DateTimeField` falls within the specified range. Here is an example:

```python
from datetime import date
from myapp.models import MyModel

start_date = date(2022, 2, 1)
end_date = date(2022, 2, 28)
results = MyModel.objects.filter(my_date_field__gte=start_date, my_date_field__lte=end_date)
```

In this example, we are filtering the `MyModel` model by the `my_date_field` field, which is a `DateTimeField`. We are using the `__gte` and `__lte` lookups to filter the results to include only those where the date of the field falls within the range of `start_date` and `end_date`.

## Section 4 - Conclusion
Filtering a `DateTimeField` in Django by a specific date or range of dates can be accomplished using the `__date`, `__gte`, and `__lte` lookups. These lookups allow you to easily filter the results based on the date or date range that you specify.
