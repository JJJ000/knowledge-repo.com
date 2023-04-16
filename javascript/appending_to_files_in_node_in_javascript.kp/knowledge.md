---
title: What is the process for adding content to a file using node?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the fs.appendFile() method to append data to a file in Node.
---

**Contents**

[TOC]

# Section 1: Setting Up

1. Import the `fs` module:

```javascript
const fs = require('fs');
```

2. Create a file path for the file you want to append to:

```javascript
const filePath = './myFile.txt';
```

# Section 2: Appending to a File

1. Open the file for writing:

```javascript
const fileHandle = fs.openSync(filePath, 'a');
```

2. Write the data to the file:

```javascript
fs.writeSync(fileHandle, 'My new data\n');
```

# Section 3: Closing the File

1. Close the file:

```javascript
fs.closeSync(fileHandle);
```

# Section 4: Verifying the Append

1. Read the file to verify the append:

```javascript
const data = fs.readFileSync(filePath);
console.log(data.toString());
```
