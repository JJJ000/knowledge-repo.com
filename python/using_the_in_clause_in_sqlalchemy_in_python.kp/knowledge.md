---
title: Sqlalchemy's in operator
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The SQLAlchemy IN clause can be used to filter a query based on a list of values in Python.
---

**Contents**

[TOC]

### Syntax
The syntax for an IN clause in SQLAlchemy is as follows: 

```
column_name.in_(list_of_values)
```

### Example
For example, if we wanted to query the table `users` for all records with the `age` column set to either 20 or 25, we could use the following statement: 

```
query = session.query(User).filter(User.age.in_([20, 25]))
```

### Result
The result of this query would be a list of all `User` objects whose `age` column is set to either 20 or 25.

### Further Considerations
It is important to note that the list of values provided to the `in_` clause should be a list of values of the same type as the column being queried. For example, if the `age` column is an integer, the list of values should be a list of integers.
