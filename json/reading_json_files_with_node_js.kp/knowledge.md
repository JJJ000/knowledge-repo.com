---
title: What is the process for loading a JSON file into a Node.js server?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `Node.js` fs module to read the JSON file into a variable, then use the `JSON.parse()` method to parse the file into a JavaScript object.
---

**Contents**

[TOC]

### Install the 'fs' Package

The 'fs' package is a Node.js core package that provides file system related operations. It can be installed using the following command:

```shell
npm install fs
```

### Read the JSON File

Once the 'fs' package is installed, the JSON file can be read using the `readFileSync` method. This method takes two parameters: the file path and the encoding type. The following example reads a JSON file located at `data.json` and sets the encoding type to `utf8`:

```javascript
const fs = require('fs');
const jsonData = fs.readFileSync('data.json', 'utf8');
```

### Parse the JSON Data

Once the JSON data is read, it needs to be parsed into a JavaScript object. This can be done using the `JSON.parse` method. The following example parses the JSON data into a JavaScript object:

```javascript
const dataObject = JSON.parse(jsonData);
```

### Access the Data

Once the JSON data is parsed into a JavaScript object, it can be accessed using dot notation. The following example accesses the `name` property of the data object:

```javascript
const name = dataObject.name;
```
