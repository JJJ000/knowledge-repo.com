---
title: Order by descending using sqlalchemy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: ORDER BY clauses can be used to sort the results of a query in descending order in SQLAlchemy by adding the keyword DESC after the column name.
---

**Contents**

[TOC]

### Section 1: Overview

SQLAlchemy is an open-source SQL toolkit and object-relational mapper (ORM) for the Python programming language. It provides a full suite of tools for working with databases, including the ability to query, manipulate, and store data. One of the most useful features of SQLAlchemy is its support for ORDER BY DESCENDING, which allows users to sort query results in descending order.

### Section 2: Syntax

The syntax for ORDER BY DESCENDING in SQLAlchemy is as follows:

```sql
SELECT [columns] 
FROM [table] 
ORDER BY [column] DESC;
```

### Section 3: Example

For example, to sort a table of customers by their last names in descending order, the following query could be used:

```sql
SELECT first_name, last_name 
FROM customers 
ORDER BY last_name DESC;
```

### Section 4: Additional Resources

For more information on ORDER BY DESCENDING in SQLAlchemy, please refer to the official documentation:

https://docs.sqlalchemy.org/en/13/core/sqlelement.html#sqlalchemy.sql.expression.OrderByClause
