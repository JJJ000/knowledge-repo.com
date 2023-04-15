---
title: What is the method for acquiring a queryset that contains all rows, with particular fields for each individual row?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the .values() method on the model queryset, passing in the specific fields you want to retrieve as arguments to the method.
---

**Contents**

[TOC]

### Section 1: Understanding QuerySets

In Python, QuerySets are used to interact with databases using built-in functions of Django ORM (Object-Relational Mapping). A QuerySet represents a collection of objects, obtained from a database, that match specific conditions.

### Section 2: The .values() method

The .values() method is used to obtain a QuerySet of specified fields for each row in the database. This method returns a QuerySet of dictionaries where the keys are the field names and the values are the corresponding values in the database.

```python
queryset = MyModel.objects.values('field1', 'field2', 'field3')
```

In the code above, MyModel is the name of the database table where the data is stored. The .values() method is used to select the fields 'field1', 'field2' and 'field3'. This method returns a QuerySet containing dictionaries, with the specified fields as keys and the corresponding values in the database as values.

### Section 3: Additional Filtering

It is also possible to apply further filtering to the QuerySet obtained using the .values() method by chaining additional methods to it.

```python
queryset = MyModel.objects.values('field1', 'field2', 'field3').filter(field1='value1')
```

In the code above, the filter() method is used to select only the rows where field1 has a value of 'value1'.

### Section 4: Conclusion

In summary, a QuerySet of specific fields for each row in the database can be obtained using the .values() method. Additional filtering can be applied to the QuerySet by chaining additional methods to it.
