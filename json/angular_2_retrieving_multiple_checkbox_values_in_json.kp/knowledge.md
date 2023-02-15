---
title: Retrieve values of multiple selected checkboxes in angular 2
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Use the `FormsModule` to bind the checked values to a model and use the `JSON.stringify()` method to convert the model to a JSON string.
---

**Contents**

[TOC]

###Section 1: Get Checkbox Values

The easiest way to get the values of multiple checked checkboxes in JSON is to use the `.map()` method. This method takes an array and creates a new array by calling a function on each element of the original array. 

In this case, the function will be used to get the value of each checked checkbox. The following example shows how to use the `.map()` method to get the value of each checked checkbox:

```
var checkboxes = document.querySelectorAll('input[type="checkbox"]:checked');
var values = Array.prototype.map.call(checkboxes, function(checkbox) {
    return checkbox.value;
});
```

###Section 2: Convert to JSON

Once the array of values has been created, it can be converted to JSON using the `JSON.stringify()` method. This method takes an object or array and converts it to a string. The following example shows how to use the `JSON.stringify()` method to convert the array of values to JSON:

```
var jsonString = JSON.stringify(values);
```

###Section 3: Output JSON

The JSON string can then be outputted and used in whatever way is necessary. The following example shows how to output the JSON string:

```
console.log(jsonString);
```

###Section 4: Example

The following example shows the entire process of getting the values of multiple checked checkboxes in JSON:

```
var checkboxes = document.querySelectorAll('input[type="checkbox"]:checked');
var values = Array.prototype.map.call(checkboxes, function(checkbox) {
    return checkbox.value;
});
var jsonString = JSON.stringify(values);
console.log(jsonString);
```
