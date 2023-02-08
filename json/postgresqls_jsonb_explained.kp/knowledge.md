---
title: An overview of jsonb in postgresql
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: JSONB is a binary format for storing JSON data in PostgreSQL, allowing for faster access and more efficient storage than the standard JSON data type.
---

**Contents**

[TOC]

# What is JSONB?
JSONB (JavaScript Object Notation Binary) is a PostgreSQL data type introduced in version 9.4. It is an extended version of the JSON data type that allows for more efficient storage and querying of JSON data. JSONB stores JSON data in a binary format which makes it more efficient to store and query than the original JSON data type.

# Advantages of JSONB
JSONB offers several advantages over the original JSON data type. It is more efficient to store and query than the original JSON data type. It also allows for indexing of JSON data, making it easier to query and retrieve specific data. Additionally, JSONB supports a wider range of data types, including dates, times, and arrays.

# Disadvantages of JSONB
Although JSONB offers several advantages over the original JSON data type, there are some drawbacks. JSONB is more complex than the original JSON data type and requires more knowledge to use. Additionally, the binary format of JSONB can be more difficult to debug and troubleshoot than the original JSON data type.

# Conclusion
JSONB is a PostgreSQL data type introduced in version 9.4 that offers more efficient storage and querying of JSON data. It is more efficient to store and query than the original JSON data type and supports a wider range of data types. However, JSONB is more complex than the original JSON data type and can be more difficult to debug and troubleshoot.
