---
title: What is the procedure for importing a JSON file using ecmascript 6?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: In ECMAScript 6, you can import a JSON file using the `import` statement.
---

**Contents**

[TOC]

# Section 1: Install Dependencies

To import a JSON file in ECMAScript 6, you need to install the following dependencies:

1. Node.js
2. NPM (Node Package Manager)

# Section 2: Create File

Create a new file in your project directory and name it `index.js`. This is where your JavaScript code will be written.

# Section 3: Import JSON File

In your `index.js` file, import your JSON file using the `import` keyword.

```
import jsonFile from './path/to/file.json';
```

# Section 4: Use JSON Data

Once the file is imported, you can use the JSON data in your code. For example, to access a specific property from the JSON data, you can use the dot notation.

```
const property = jsonFile.propertyName;
```
