---
title: Retrieve data from spring crudrepository using a list of inventory ids that correspond to the in clause
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, Spring CrudRepository findByInventoryIds is equivalent to IN clause in Java.
---

**Contents**

[TOC]

## Overview
The `findByInventoryIds` method of the Spring CrudRepository is a query method used to retrieve data from a repository based on a list of inventory IDs. This method is equivalent to the `IN` clause in Java, which is used to compare values in a specific set of values.

## What is the IN Clause?
The `IN` clause in Java is a comparison operator used to compare values in a specific set of values. It is used to determine if a value is in the set of values specified in the `IN` clause. For example, the following statement would return all rows where the value of the `name` column is either `John` or `Paul`:

```
SELECT * FROM table WHERE name IN ('John', 'Paul');
```

## What is Spring CrudRepository findByInventoryIds()?
The `findByInventoryIds` method of the Spring CrudRepository is a query method used to retrieve data from a repository based on a list of inventory IDs. This method is equivalent to the `IN` clause in Java, as it is used to determine if a value is in the set of values specified in the `findByInventoryIds` argument. For example, the following statement would return all rows where the value of the `inventory_id` column is in the list of inventory IDs provided in the argument:

```
SELECT * FROM table WHERE inventory_id IN (list of inventory ids);
```

## Conclusion
The `findByInventoryIds` method of the Spring CrudRepository is equivalent to the `IN` clause in Java, as it is used to determine if a value is in the set of values specified in the argument. This method is useful for retrieving data from a repository based on a list of inventory IDs.
