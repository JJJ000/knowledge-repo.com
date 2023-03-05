---
title: Modify the data in the JSON file (updating files)
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: It is possible to change values in a JSON file by reading it, modifying the desired value and then writing it back to the file.
---

**Contents**

[TOC]

# Introduction
JavaScript Object Notation (JSON) is a lightweight format for storing and exchanging data. It is commonly used for data transmission between client-server applications. JSON data is represented as key-value pairs and can be easily manipulated using various programming languages. In this article, we will discuss how to change values in a JSON file using JavaScript.

# Reading the JSON File
Before we can modify values in a JSON file, we need to read the data from the file. In JavaScript, we can read the data from a JSON file using the `fs` module. The following code snippet demonstrates how to read data from a JSON file:

```javascript
const fs = require('fs');

// Read the JSON data from the file
fs.readFile('data.json', 'utf8', (err, data) => {
  if (err) throw err;

  // Parse the JSON data into an object
  const jsonData = JSON.parse(data);

  // Modify the data
  jsonData.name = 'John Doe';

  // Write the modified data back to the file
  fs.writeFile('data.json', JSON.stringify(jsonData), (err) => {
    if (err) throw err;
    console.log('Data written to file');
  });
});
```

# Modifying the Values
Once we have read the JSON data from the file, we can modify the values in the object. JavaScript provides various methods for modifying objects such as `Object.assign()`, `Object.keys()`, etc. The following code snippet demonstrates how to modify the `name` property of a JSON object:

```javascript
const fs = require('fs');

// Read the JSON data from the file
fs.readFile('data.json', 'utf8', (err, data) => {
  if (err) throw err;

  // Parse the JSON data into an object
  const jsonData = JSON.parse(data);

  // Modify the data
  jsonData.name = 'John Doe';

  // Write the modified data back to the file
  fs.writeFile('data.json', JSON.stringify(jsonData), (err) => {
    if (err) throw err;
    console.log('Data written to file');
  });
});
```

In the above code snippet, we have modified the `name` property of the `jsonData` object to `'John Doe'`. We can modify any property in a similar way.

# Writing the Modified Data
After modifying the data, we need to write the modified data back to the JSON file. To write data to a file in Node.js, we can use the `fs.writeFile()` method. The following code snippet demonstrates how to write the modified JSON data back to the file:

```javascript
const fs = require('fs');

// Read the JSON data from the file
fs.readFile('data.json', 'utf8', (err, data) => {
  if (err) throw err;

  // Parse the JSON data into an object
  const jsonData = JSON.parse(data);

  // Modify the data
  jsonData.name = 'John Doe';

  // Write the modified data back to the file
  fs.writeFile('data.json', JSON.stringify(jsonData), (err) => {
    if (err) throw err;
    console.log('Data written to file');
  });
});
```

In the above code snippet, we have used the `fs.writeFile()` method to write the modified `jsonData` object back to the file in JSON format. We have used the `JSON.stringify()` method to convert the object into a JSON string before writing it to the file.

# Conclusion
In this article, we have discussed how to change values in a JSON file using JavaScript. We have seen how to read the JSON data from the file, modify the values in the object, and write the modified data back to the file. JavaScript provides various methods for working with objects, which can be used to modify the data in a JSON file.
