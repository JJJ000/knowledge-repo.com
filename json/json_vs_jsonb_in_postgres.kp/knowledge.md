---
title: What is the distinction between JSON and jsonb data types in postgres?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: JSON stores data as a string, while JSONB stores data as binary objects, allowing for more efficient storage and querying.
---

**Contents**

[TOC]

# JSON
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is easy for humans to read and write, and for machines to parse and generate. JSON is a text-based format that is language independent and is often used for transmitting data over a network connection.

# JSONB
JSONB (JavaScript Object Notation Binary) is a binary representation of JSON data. It is optimized for storing and querying data in PostgreSQL. Unlike JSON, JSONB stores data in a decomposed binary format which allows for faster access and better space utilization.

# Differences
1. Storage Format: JSON is a text-based format while JSONB is a binary format.
2. Querying: JSONB is optimized for querying data and can be queried using the same SQL syntax used for querying other data types. JSON data can be queried using standard JSON functions.
3. Indexing: JSONB supports indexing while JSON does not.
4. Space Utilization: JSONB is more space efficient than JSON as it stores data in a decomposed binary format.
