---
title: Transform a standard Java array or arraylist into a JSON array in an Android environment
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: You can use the Gson library to convert a Java Array or ArrayList to a JSON Array in Android.
---

**Contents**

[TOC]

### Section 1: Using Gson Library 

Gson is a Java library that can be used to convert Java Objects into their JSON representation. It can also be used to convert a JSON string to an equivalent Java object.

To convert a normal Java Array or ArrayList to a JSON Array, we can use the toJson() method of the Gson class.

### Section 2: Example

Here is an example of how to convert an ArrayList of Strings to a JSON Array:

```
//Create an ArrayList of Strings
ArrayList<String> list = new ArrayList<String>();
list.add("item1");
list.add("item2");
list.add("item3");

//Create Gson object
Gson gson = new Gson();

//Convert the ArrayList to a JSON Array
JsonArray jsonArray = gson.toJsonTree(list).getAsJsonArray();

//Print the JSON Array
System.out.println(jsonArray.toString());
```

### Section 3: Output

The output of the above code will be:

```
[
  "item1",
  "item2",
  "item3"
]
```

### Section 4: Conclusion

Using the Gson library, we can easily convert a normal Java Array or ArrayList to a JSON Array. This is a useful tool for working with JSON data in Android applications.
