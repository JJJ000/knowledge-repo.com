---
title: What is the process for transforming a csv file into a JSON object using node.js?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Node.js can be used to convert CSV to JSON using the `csvtojson` package.
---

**Contents**

[TOC]

### 1. Install csvtojson

First, install the csvtojson package. This package is a parser converting CSV text input into JSON.

```
npm install csvtojson
```

### 2. Create Converter

Create a converter instance with the following code:

```
const csvFilePath = '<path to csv file>';
const csv = require('csvtojson');
const converter = csv({
    noheader: false,
    output: "json"
});
```

### 3. Convert CSV to JSON

Call the fromFile() method of the converter instance to convert the CSV data to JSON.

```
converter.fromFile(csvFilePath, (err, result) => {
    if (err) {
        console.log("An Error Has Occurred");
    }
    console.log(result);
});
```

### 4. Output JSON

The result of the conversion will be output to the console in JSON format.
