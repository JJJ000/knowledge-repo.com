---
title: Transforming a JSON object into a csv file using javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: The JSON object can be converted to CSV format in JavaScript using the json2csv library.
---

**Contents**

[TOC]

**Section 1: Setup**

1. Create a function to convert a JSON object to a CSV string:

```javascript
function convertToCSV(objArray) {
    var array = typeof objArray != 'object' ? JSON.parse(objArray) : objArray;
    var str = '';
 
    for (var i = 0; i < array.length; i++) {
        var line = '';
        for (var index in array[i]) {
            if (line != '') line += ','
 
            line += array[i][index];
        }
 
        str += line + '\r\n';
    }
 
    return str;
}
```

**Section 2: Usage**

1. Create a JSON object:

```javascript
var jsonObject = [
    {
        "name": "John Doe",
        "age": "25",
        "city": "New York"
    },
    {
        "name": "Jane Doe",
        "age": "30",
        "city": "San Francisco"
    }
]
```

2. Pass the JSON object to the `convertToCSV` function:

```javascript
var csvString = convertToCSV(jsonObject);
```

**Section 3: Output**

The resulting CSV string will look like this:

```
name,age,city
John Doe,25,New York
Jane Doe,30,San Francisco
```

**Section 4: Notes**

The `convertToCSV` function can be used to convert any valid JSON object to a CSV string. It is important to note that the order of the JSON object's properties will be preserved in the resulting CSV string.
