---
title: What is the syntax for retrieving nested elements from a JSON object using the getjsonarray method?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the getJSONArray() method to access nested elements of a JSON object.
---

**Contents**

[TOC]

## Section 1: Understanding getJSONArray

getJSONArray is a method used to access JSONArray objects from a JSONObject. It is a method of the JSONObject class, and can be used to access a JSONArray object from a JSONObject.

## Section 2: Accessing Nested Elements

When accessing nested elements of a JSONObject, the getJSONArray method can be used to access the nested elements. To do this, the name of the object that contains the nested elements must be provided as an argument to the getJSONArray method. This will return the JSONArray object associated with the given name.

## Section 3: Iterating Through the Nested Elements

Once the JSONArray object has been retrieved, it can be iterated through to access the individual elements. This can be done using a for loop, as shown below:

```
JSONArray array = jsonObject.getJSONArray("name");
for (int i = 0; i < array.length(); i++) {
    JSONObject nestedObject = array.getJSONObject(i);
    // Access individual elements here
}
```

## Section 4: Example

For example, consider the following JSON object:

```
{
  "name": "John",
  "age": 30,
  "address": {
    "street": "Main Street",
    "city": "New York"
  }
}
```

To access the address elements, we can use the getJSONArray method as follows:

```
JSONObject jsonObject = new JSONObject(jsonString);
JSONArray addressArray = jsonObject.getJSONArray("address");

for (int i = 0; i < addressArray.length(); i++) {
    JSONObject addressObject = addressArray.getJSONObject(i);
    String street = addressObject.getString("street");
    String city = addressObject.getString("city");
    // Do something with the street and city values
}
```
