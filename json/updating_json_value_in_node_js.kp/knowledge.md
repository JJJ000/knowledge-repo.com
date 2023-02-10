---
title: What is the process for updating a value in a JSON file and saving it using node.js?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the `fs` module to read the JSON file, modify the value, and then use the `fs` module to write the JSON file back to disk.
---

**Contents**

[TOC]

# Section 1: Read JSON File

In order to update a value in a JSON file and save it through Node.js, the first step is to read the JSON file. This can be done using the `fs` module:

```javascript
const fs = require('fs');
const data = fs.readFileSync('path/to/file.json');
const jsonData = JSON.parse(data);
```

# Section 2: Update Value

Once the JSON file has been read, the next step is to update the desired value. This can be done by simply assigning a new value to the desired key in the `jsonData` object:

```javascript
jsonData.key = newValue;
```

# Section 3: Stringify JSON

After updating the value, the JSON object must be stringified in order to write it to the file:

```javascript
const jsonString = JSON.stringify(jsonData);
```

# Section 4: Write to File

Finally, the stringified JSON can be written to the file using the `fs` module:

```javascript
fs.writeFileSync('path/to/file.json', jsonString);
```
