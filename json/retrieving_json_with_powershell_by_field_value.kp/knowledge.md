---
title: Retrieve a JSON object in powershell using a field value
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use the Select-Object cmdlet to filter a JSON object by field value.
---

**Contents**

[TOC]

## Using ConvertFrom-Json

The `ConvertFrom-Json` cmdlet can be used to retrieve a JSON object by field value. It works by taking a string of JSON data as input, parsing it and returning a PowerShell object.

To use `ConvertFrom-Json` to retrieve a JSON object by field value, the following steps can be followed:

1. Create a string containing the JSON data.
2. Use the `ConvertFrom-Json` cmdlet to parse the JSON data and convert it into a PowerShell object.
3. Use the `Select-Object` cmdlet to filter the PowerShell object based on the desired field value.

## Example

The following example demonstrates how to use `ConvertFrom-Json` to retrieve a JSON object by field value.

```powershell
$jsonData = '{
    "name": "John Doe",
    "age": 25,
    "city": "New York"
}'

$jsonObject = ConvertFrom-Json $jsonData
$jsonObject | Select-Object -Property Name, Age -ExpandProperty City -eq 'New York'
```

The above example will return the following object:

```
Name Age City
---- --- ----
John Doe 25 New York
```
