---
title: What is the process for extracting data from an excel (xls) file using javascript/html5?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: You can use the SheetJS library to parse an Excel (XLS) file in Javascript/HTML5 and output it as JSON.
---

**Contents**

[TOC]

## Section 1: Prerequisites

Before you can parse an Excel (XLS) file in Javascript/HTML5, there are a few things you need to have in place:

1. An HTML page with a script tag for the Javascript code.
2. The Excel file you want to parse.
3. A library for parsing the Excel file, such as SheetJS.

## Section 2: Setting Up the HTML File

In your HTML page, add a script tag to include the SheetJS library.

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.15.2/xlsx.full.min.js"></script>
```

## Section 3: Reading the Excel File

Once the SheetJS library is included in the HTML page, you can use the `XLSX.read()` function to read the Excel file.

```javascript
var workbook = XLSX.read(file, {type:'binary'});
```

The `workbook` variable now contains the data from the Excel file.

## Section 4: Parsing the Excel File

Once the Excel file is read, you can use the `XLSX.utils.sheet_to_json()` function to parse the data into a JSON object.

```javascript
var jsonData = XLSX.utils.sheet_to_json(workbook.Sheets[workbook.SheetNames[0]]);
```

The `jsonData` variable now contains the data from the Excel file in JSON format.
