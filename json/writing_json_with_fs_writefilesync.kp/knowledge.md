---
title: Saving a JSON object to a file using fs.writefilesync
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: fs.writeFileSync(`filename.json`, JSON.stringify(jsonObject));
---

**Contents**

[TOC]

##### Step 1: Import fs

At the top of the file, import the fs module.

```javascript
const fs = require('fs');
```

##### Step 2: Create JSON Object

Create a JSON object that you would like to save to a file.

```javascript
const data = {
  name: 'John Doe',
  age: 30,
  city: 'New York'
};
```

##### Step 3: Convert to String

Convert the JSON object to a string using the `JSON.stringify()` method.

```javascript
const jsonString = JSON.stringify(data);
```

##### Step 4: Write to File

Use the `fs.writeFileSync()` method to write the JSON string to a file.

```javascript
fs.writeFileSync('data.json', jsonString);
```
