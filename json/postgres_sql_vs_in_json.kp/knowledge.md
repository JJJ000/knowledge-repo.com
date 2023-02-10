---
title: What is the distinction between the "->>" and "->" operators in Postgres sql?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: `->>` is used to access the value of a key in a JSON object, while `->` is used to access elements of a JSON array.
---

**Contents**

[TOC]

#### `->>` 
`->>` is used to extract the value of a specified key in a JSON string. It returns the value in text format.

#### `->` 
`->` is used to extract the value of a specified key in a JSON string. It returns the value in JSON data type.

#### Difference
The main difference between `->>` and `->` is the return type. `->>` returns the value in text format while `->` returns the value in JSON data type.
