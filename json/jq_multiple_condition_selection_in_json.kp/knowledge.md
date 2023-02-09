---
title: Jq select multiple criteria
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: In JSON, multiple conditions can be selected using logical operators such as `AND` and `OR`.
---

**Contents**

[TOC]

**Section 1: Basic Syntax**

The basic syntax for selecting multiple conditions in JSON is to use the logical operator `AND` or `OR` to combine multiple conditions. For example, the following syntax can be used to select all records with a field `name` equal to `John` and `age` greater than `20`:

```
SELECT * FROM table WHERE name = 'John' AND age > 20
```

**Section 2: Nested Queries**

It is also possible to use nested queries to select multiple conditions in JSON. Nested queries are queries that are nested within other queries. For example, the following syntax can be used to select all records with a field `name` equal to `John` and `age` greater than `20`:

```
SELECT * FROM table WHERE (name = 'John' OR age > 20)
```

**Section 3: Subqueries**

Subqueries are another way to select multiple conditions in JSON. Subqueries are queries that are executed within another query. For example, the following syntax can be used to select all records with a field `name` equal to `John` and `age` greater than `20`:

```
SELECT * FROM table WHERE name = (SELECT name FROM table WHERE age > 20)
```

**Section 4: Wildcard Queries**

Wildcard queries can also be used to select multiple conditions in JSON. Wildcard queries are queries that use the `LIKE` operator to match patterns. For example, the following syntax can be used to select all records with a field `name` equal to `John` and `age` greater than `20`:

```
SELECT * FROM table WHERE name LIKE 'John%' AND age > 20
```
