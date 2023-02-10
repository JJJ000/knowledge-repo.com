---
title: How can I convert a JSON array into separate rows in a postgresql database?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the JSON\_ARRAY\_ELEMENTS() function to extract the elements from the JSON array and insert them into rows in Postgres.
---

**Contents**

[TOC]

### Section 1: Setting Up the Table

1. Create a table in Postgres with the following columns:
   - `id` (integer)
   - `data` (jsonb)

2. Insert the JSON array into the `data` column.

### Section 2: Parsing the JSON Array

1. Use the `jsonb_array_elements` function to extract the individual elements from the array.

2. Create a `SELECT` statement to retrieve the elements from the `data` column.

### Section 3: Inserting the Elements into Rows

1. Use the `INSERT INTO` statement to insert the elements into the table.

2. Use the `SELECT` statement from the previous step to retrieve the elements.

### Section 4: Updating the Table

1. Use the `UPDATE` statement to update the `id` column with a unique identifier for each row.

2. Use the `SELECT` statement to retrieve the updated data.
