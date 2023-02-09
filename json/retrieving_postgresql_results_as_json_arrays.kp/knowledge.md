---
title: What is the output of a postgresql query when expressed as a JSON array?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, PostgreSQL can return a result set as a JSON array.
---

**Contents**

[TOC]

## Section 1: Overview
PostgreSQL is an open source database management system that supports the storage of data in a variety of formats, including JSON. PostgreSQL can return the result set of a query as a JSON array, allowing the data to be easily consumed by other applications.

## Section 2: How to Return Results as JSON
In order to return the result set of a query as a JSON array, the query must be written using the `json_agg` function. This function will aggregate the rows of the result set into a single JSON array. The following example shows how to use the `json_agg` function to return the result set of a query as a JSON array:

```sql
SELECT json_agg(t)
FROM (
    SELECT *
    FROM table_name
) t;
```

## Section 3: Limitations
It is important to note that the `json_agg` function will only return the result set as a JSON array. It will not return the result set as a JSON object. Additionally, the `json_agg` function will not work on binary or large object (BLOB) data types.

## Section 4: Conclusion
PostgreSQL can return the result set of a query as a JSON array, allowing the data to be easily consumed by other applications. The `json_agg` function can be used to aggregate the rows of the result set into a single JSON array. However, it is important to note that the `json_agg` function will not work on binary or large object (BLOB) data types.
