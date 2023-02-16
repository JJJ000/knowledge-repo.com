---
title: What is the procedure for importing a JSON file into postgresql?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: You can use the PostgreSQL command line tool `COPY` to import a JSON file into PostgreSQL.
---

**Contents**

[TOC]

### Step 1: Create a Table

First, create a table in PostgreSQL with the same fields as the JSON file. You can do this by running the following SQL command:

```
CREATE TABLE table_name (
    field1 data_type, 
    field2 data_type, 
    ...
);
```

Where `table_name` is the name of the table and `field1`, `field2`, etc. are the names of the fields in the table and `data_type` is the type of data that will be stored in each field (e.g. text, integer, etc.).

### Step 2: Import the JSON File

Next, you can use the `\copy` command to import the JSON file into the table you just created. This command takes the following form:

```
\copy table_name FROM 'file_name.json' WITH (FORMAT JSON);
```

Where `table_name` is the name of the table you created and `file_name.json` is the name of the JSON file you want to import.

### Step 3: Verify the Data

Finally, you can use the `SELECT` command to verify that the data from the JSON file was imported correctly. This command takes the following form:

```
SELECT * FROM table_name;
```

Where `table_name` is the name of the table you created. This will display all of the data from the table, which should include the data from the JSON file.
