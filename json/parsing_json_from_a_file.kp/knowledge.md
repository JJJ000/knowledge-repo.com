---
title: Retrieving JSON from a file
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the json.load() method to read JSON from a file.
---

**Contents**

[TOC]

1. **Create the JSON Object**

To read JSON from a file, first create a JSON object. The file can be read using the `fs` module in Node.js, or the `FileReader` in the browser.

2. **Read the File**

Once the JSON object is created, the file can be read using the `fs.readFile` or `FileReader.readAsText` methods. The file should be read as a UTF-8 string.

3. **Parse the JSON**

Once the file is read, the JSON can be parsed using the `JSON.parse` method. This will return an object that can be used to access the data in the JSON file.

4. **Access the Data**

Once the JSON is parsed, the data can be accessed using the object created from the `JSON.parse` method. The data can then be used to create new objects, manipulate existing data, or whatever else is needed.
