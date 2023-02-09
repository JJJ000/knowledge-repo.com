---
title: What is the process for transforming formdata (html5 object) into json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the FormData.entries() method to convert FormData to JSON.
---

**Contents**

[TOC]

**Section 1: Create FormData Object**

FormData objects can be created using the FormData constructor. The constructor takes one argument, which is an HTML form element, and returns a FormData object.

```
let formElement = document.querySelector('form');
let formData = new FormData(formElement);
```

**Section 2: Iterate Through FormData Object**

FormData objects are iterable, meaning they can be looped through with the `for...of` statement.

```
let json = {};
for (let [key, value] of formData) {
  json[key] = value;
}
```

**Section 3: Stringify JSON**

Once the FormData object has been iterated through and the JSON object has been created, the JSON object can be stringified using the `JSON.stringify` method.

```
let jsonString = JSON.stringify(json);
```

**Section 4: Output JSON String**

The JSON string can be outputted to the console or stored in a variable for future use.

```
console.log(jsonString);
```
