---
title: What is the best way to display a JSON string as a table using jq?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: jq can be used to format a JSON string as a table by using the `.table` command.
---

**Contents**

[TOC]

### Section 1: Install jq

In order to format a JSON string as a table using jq, you must first install jq. jq is a command-line JSON processor. You can install jq on Linux, macOS, and Windows. 

### Section 2: Create JSON String

Create a JSON string that you want to format as a table. For example: 

```
{
  "name": "John Doe",
  "age": "35",
  "location": "New York City"
}
```

### Section 3: Format JSON String as Table

Use the jq command to format the JSON string as a table: 

```
jq -r '["Name", "Age", "Location"], [.name, .age, .location] | @tsv'
```

This will output the following table: 

```
Name	Age	Location
John Doe	35	New York City
```

### Section 4: Output Table to File

If you want to output the table to a file, you can add the -o option to the jq command: 

```
jq -r '["Name", "Age", "Location"], [.name, .age, .location] | @tsv' -o output.tsv
```

This will output the table to a file named `output.tsv`.
