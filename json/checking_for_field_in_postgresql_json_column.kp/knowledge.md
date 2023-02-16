---
title: Verify if a field is present in a postgresql column of JSON type
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Yes, PostgreSQL supports querying values within a JSON type column.
---

**Contents**

[TOC]

## Section 1 - Using JSONB
PostgreSQL 9.4 and above provides the `JSONB` data type, which stores the JSON data in a binary format. The `JSONB` data type provides functions to check if a field exists in a JSON type column. 

## Section 2 - Using Operators
The `JSONB` data type provides operators such as `?`, `?|`, and `?&` to check if a field exists in a JSON type column. The `?` operator checks if the specified field exists in the JSON object. The `?|` operator checks if any of the specified fields exist in the JSON object. The `?&` operator checks if all of the specified fields exist in the JSON object. 

## Section 3 - Using Functions
The `JSONB` data type also provides functions such as `jsonb_exists` and `jsonb_typeof` to check if a field exists in a JSON type column. The `jsonb_exists` function checks if the specified field exists in the JSON object. The `jsonb_typeof` function checks the data type of the specified field in the JSON object.

## Section 4 - Using Paths
The `JSONB` data type also provides paths to check if a field exists in a JSON type column. The `#>>` operator is used to access the value of a field in a JSON object. The `#>` operator is used to check if a field exists in a JSON object.
