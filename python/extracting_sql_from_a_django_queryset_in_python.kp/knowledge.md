---
title: Retrieving the sql generated from a django queryset
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can get the SQL from a Django QuerySet by using the QuerySet`s `.query` attribute.
---

**Contents**

[TOC]

1. Overview 

2. Using `.query` 

3. Using `.explain()` 

4. Using `.get_compiler()` 

## 1. Overview 

Django is an open source web framework written in Python that allows developers to create dynamic web applications. It is built on the popular Model-View-Template (MTV) architecture, which helps developers create web applications quickly and easily. As part of the MTV architecture, Django provides an object-relational mapper (ORM) that allows developers to interact with databases using Python code. This ORM provides a powerful QuerySet API that allows developers to query the database and retrieve the data they need. 

In some cases, developers may need to get the raw SQL query from a Django QuerySet. This can be useful for debugging or for analyzing the query performance. In this tutorial, we will discuss the different ways of getting the SQL from a Django QuerySet in Python. 

## 2. Using `.query` 

The most straightforward way to get the SQL from a Django QuerySet is to use the `.query` attribute. This attribute contains the actual SQL query that is used to retrieve the data from the database. It is important to note that the `.query` attribute is only available after the query has been executed. 

For example, if we have a QuerySet called `qs`, we can get the SQL query by simply printing the `.query` attribute:

```python
print(qs.query)
```

## 3. Using `.explain()` 

Another way to get the SQL from a Django QuerySet is to use the `.explain()` method. This method prints out the execution plan of the SQL query, which can be useful for debugging and analyzing query performance.

For example, if we have a QuerySet called `qs`, we can get the execution plan of the SQL query by simply calling the `.explain()` method:

```python
qs.explain()
```

## 4. Using `.get_compiler()` 

The last way to get the SQL from a Django QuerySet is to use the `.get_compiler()` method. This method returns the SQL compiler object for the QuerySet, which contains the actual SQL query. 

For example, if we have a QuerySet called `qs`, we can get the SQL query by calling the `.get_compiler()` method and then accessing the `.as_sql()` attribute:

```python
sql_query = qs.get_compiler().as_sql()
```
