---
title: What is the process for transforming JSON data into a csv format and storing it in a variable?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use the json.dumps() method to convert a JSON object to a CSV string and store it in a variable.
---

**Contents**

[TOC]

# Section 1: Install the Required Packages

In order to convert JSON to CSV format, we need to install the [json2csv](https://www.npmjs.com/package/json2csv) package. This can be done by running the following command in the terminal: 

`npm install json2csv`

# Section 2: Import the Package

Once the package is installed, we can import it in our code. This can be done by adding the following line: 

`const json2csv = require('json2csv');`

# Section 3: Convert JSON to CSV

Now, we can use the `json2csv` function to convert the JSON data to CSV format. The following code snippet shows how this can be done: 

```
const fields = ['field1', 'field2', 'field3'];
const opts = { fields };

try {
  const csv = json2csv.parse(myData, opts);
  console.log(csv);
} catch (err) {
  console.error(err);
}
```

# Section 4: Store in a Variable

Once the JSON data is converted to CSV format, we can store it in a variable. This can be done by simply assigning the `csv` variable to another variable, as shown below: 

`const csvData = csv;`
