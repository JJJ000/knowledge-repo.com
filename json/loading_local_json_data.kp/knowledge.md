---
title: Store the contents of a local JSON file in a variable
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use the `fetch` API to load a local JSON file into a variable.
---

**Contents**

[TOC]

##### Step 1: Create a Variable

Create a variable to store the JSON data.

```javascript
let myJSONData;
```

##### Step 2: Read File

Use the `fs` module to read the local JSON file.

```javascript
const fs = require('fs');

fs.readFile('path/to/file.json', (err, data) => {
    if (err) {
        console.log(err);
    } else {
        myJSONData = JSON.parse(data);
    }
});
```

##### Step 3: Use Data

Once the file has been read and parsed, the data can be used.

```javascript
console.log(myJSONData);
```
