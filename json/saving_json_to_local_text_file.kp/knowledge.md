---
title: What is the process for writing a JSON file to a local text file?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the `JSON.stringify()` method to convert the JSON object to a string, and then use the `fs.writeFile()` method to write the string to a local text file.
---

**Contents**

[TOC]

# Section 1: Create a JSON Object

The first step is to create a JSON object that will be saved to the local text file. This can be done by declaring a variable and assigning it a value that contains the JSON data. For example:

```
let jsonObject = {
    "name": "John Smith",
    "age": 30,
    "address": "123 Main Street"
};
```

# Section 2: Stringify the JSON Object

The next step is to stringify the JSON object so that it can be written to a file. This can be done using the `JSON.stringify()` method. The syntax for this method is as follows:

```
let jsonString = JSON.stringify(jsonObject);
```

# Section 3: Write the String to a File

The last step is to write the stringified JSON object to a file. This can be done using the `fs.writeFile()` method. The syntax for this method is as follows:

```
fs.writeFile('filename.txt', jsonString, (err) => {
    if (err) throw err;
    console.log('The file has been saved!');
});
```

# Section 4: Read the File

Once the file has been saved, it can be read using the `fs.readFile()` method. The syntax for this method is as follows:

```
fs.readFile('filename.txt', (err, data) => {
    if (err) throw err;
    let jsonData = JSON.parse(data);
    console.log(jsonData);
});
```

The `jsonData` variable will contain the parsed JSON object that was saved to the file.
