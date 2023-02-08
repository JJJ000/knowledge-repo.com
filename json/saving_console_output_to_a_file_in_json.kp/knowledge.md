---
title: What is the process for writing the output of a console.log(object) to a file?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can use the fs module in Node.js to write the output of a console.log(object) to a file in JSON format.
---

**Contents**

[TOC]

## Section 1: Set up the console

1. Open the console in your text editor of choice.
2. Create a variable that will store the object you want to save in JSON format.

## Section 2: Stringify the Object

1. Use the `JSON.stringify()` method to convert the object into a string.
2. Store the stringified object in a new variable.

## Section 3: Create a File

1. Use the `fs` module to create a new file.
2. Specify the file name and extension.

## Section 4: Write to the File

1. Use the `fs.writeFile()` method to write the stringified object to the file.
2. Specify the file name and the stringified object.
3. Save the file.
