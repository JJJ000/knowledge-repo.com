---
title: Using javascript, add a new key-value pair to a JSON object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can add a new attribute (element) to a JSON object using JavaScript by simply assigning a new key-value pair to the object.
---

**Contents**

[TOC]

### Step 1: Accessing the Object

In order to add a new attribute to an existing JSON object, we must first access the object. To do this, we can use the `JSON.parse()` method to convert the JSON string into a JavaScript object.

### Step 2: Adding the Attribute

Once we have the object, we can add the new attribute to it using the `object.attribute = value` syntax. For example, if we wanted to add an "age" attribute to an existing object, we would write `object.age = 25`.

### Step 3: Converting the Object Back to a String

Once we have added the new attribute, we need to convert the object back to a JSON string. To do this, we can use the `JSON.stringify()` method.

### Step 4: Updating the JSON

Finally, we need to update the original JSON with the new object. To do this, we can use the `JSON.stringify()` method to convert the updated object back into a JSON string and then update the original JSON with the new string.
