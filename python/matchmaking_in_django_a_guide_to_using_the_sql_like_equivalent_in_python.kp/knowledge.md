---
title: How to express the sql "like" operator in a django query?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The equivalent of `LIKE` in Django query is `\_\_contains`.
---

**Contents**

[TOC]

## Section 1: Introduction to LIKE in SQL

In SQL, "LIKE" is a keyword used to search for a specified pattern in a string. It is commonly used in conjunction with the "%" wildcards to match any sequence of characters.

For example, the following query would return all rows from the "users" table where the "name" column contains the sequence of characters "John":

```
SELECT * FROM users WHERE name LIKE '%John%';
```


## Section 2: Django QuerySet syntax for LIKE

In Django, the equivalent of the "LIKE" keyword is the "__icontains" lookup. This allows you to search for a specified pattern in a string regardless of capitalization. The "__contains" lookup can also be used for case-sensitive searches.

For example, the following Django QuerySet would return all objects from the "User" model where the "name" field contains the sequence of characters "John". It is case-insensitive.

```
User.objects.filter(name__icontains='john')
```


## Section 3: Using wildcards in Django query

To use wildcards in Django QuerySets, you can combine "__icontains" or "__contains" with the "Q" (for queries) object and the "~" operator.

The following example would return all objects from the "User" model where the name field starts with "John" and ends with "Doe" (regardless of characters in between):

```
from django.db.models import Q

User.objects.filter(Q(name__icontains='John') & Q(name__icontains='Doe'))
```


## Section 4: Conclusion

In conclusion, the Django QuerySet equivalent of the SQL "LIKE" keyword is the "__icontains" or "__contains" lookup. Wildcards can be used in combination with the "Q" object and the "~" operator. These tools allow you to write powerful search queries in Python without having to revert to SQL.
