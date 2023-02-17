---
title: Use node to process xlsx files and generate json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: You can use the `xlsx` npm package to parse XLSX files and create JSON objects.
---

**Contents**

[TOC]

### Section 1: Prerequisites

Before you can parse an XLSX file with Node, you need to install a few packages. The most popular one is the [xlsx](https://www.npmjs.com/package/xlsx) package. This package provides a JavaScript API for reading and writing data in XLSX files.

### Section 2: Parsing the XLSX File

Once you have the xlsx package installed, you can use it to parse the XLSX file. To do this, you need to first read the file into a JavaScript object. You can do this using the `readFile` method provided by the xlsx package. This method takes the path to the file as an argument and returns an object containing the data from the file.

Once you have the data in a JavaScript object, you can use the `utils.sheet_to_json` method provided by the xlsx package to convert the data into a JSON object. This method takes the data object as an argument and returns a JSON object containing the data from the file.

### Section 3: Writing the JSON File

Once you have the JSON object, you can use the `writeFile` method provided by the xlsx package to write the data to a file. This method takes the path to the file and the JSON object as arguments and writes the data to the file.

### Section 4: Conclusion

Parsing an XLSX file with Node and creating a JSON file is a fairly simple process. All you need to do is install the xlsx package, read the XLSX file into a JavaScript object, convert the data to a JSON object, and then write the data to a file. With this process, you can easily parse an XLSX file and create a JSON file.
