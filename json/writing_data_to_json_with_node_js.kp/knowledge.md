---
title: Add data to a JSON file using node.js
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Node.js can be used to write/add data to a JSON file using the fs.writeFile() method.
---

**Contents**

[TOC]

# Section 1: Read the JSON File

To write or add data to a JSON file using Node.js, the first step is to read the existing JSON file. This can be done using the `fs` module and the `readFile` method. 

```
var fs = require('fs');

fs.readFile('data.json', 'utf8', function (err, data) {
    if (err) throw err;
    var jsonData = JSON.parse(data);
});
```

# Section 2: Add Data to the JSON File

Once the file is read, data can be added to the JSON object. This can be done by simply adding the new data to the existing JSON object.

```
jsonData.newData = 'This is new data';
```

# Section 3: Write the JSON File

Once the data is added to the JSON object, the file can be written back to the disk using the `writeFile` method.

```
fs.writeFile('data.json', JSON.stringify(jsonData), 'utf8', function (err) {
    if (err) throw err;
    console.log('Data is saved');
});
```

# Section 4: Final Result

The final result of this process is a JSON file with the newly added data.

```
{
    "existingData": "This is existing data",
    "newData": "This is new data"
}
```
