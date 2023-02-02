---
title: What is the syntax for an or condition in a django queryset?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the `|` operator to perform an OR condition in a Django queryset.
---

**Contents**

[TOC]

##### Using Q Objects

The Q object in Django allows us to build complex queries with multiple conditions. The OR condition can be achieved by using the Q object's `|` operator.

For example, the following query will return all the objects with `name` either `John` or `Jane`:

```python
MyModel.objects.filter(Q(name='John') | Q(name='Jane'))
```

##### Using Django ORM

The Django ORM also supports the OR condition using the `|` operator.

For example, the following query will return all the objects with `name` either `John` or `Jane`:

```python
MyModel.objects.filter(name='John' | name='Jane')
```

##### Using SQL

The OR condition can also be used in raw SQL queries.

For example, the following query will return all the objects with `name` either `John` or `Jane`:

```sql
SELECT * FROM my_model WHERE name = 'John' OR name = 'Jane'
```
