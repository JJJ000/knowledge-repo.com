---
title: Transform an arraylist of mycustomclass objects into a jsonarray
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use the Gson library to convert an ArrayList of MyCustomClass objects to a JSONArray.
---

**Contents**

[TOC]

##### Section 1: Create JSONObject

We can convert an `ArrayList<MyCustomClass>` to a `JSONArray` by creating a `JSONObject` for each item in the `ArrayList`. We can do this by looping through the `ArrayList` and creating a `JSONObject` for each item. 

##### Section 2: Add Data to JSONObject

For each `JSONObject`, we can add the data from the corresponding `MyCustomClass` object. We can do this by accessing the fields of the `MyCustomClass` object and setting the corresponding values in the `JSONObject`. 

##### Section 3: Add JSONObjects to JSONArray

Once we have created a `JSONObject` for each item in the `ArrayList`, we can add them to a `JSONArray`. We can do this by looping through the `ArrayList` and adding each `JSONObject` to the `JSONArray`.

##### Section 4: Return JSONArray

Finally, we can return the `JSONArray` which contains all of the `JSONObjects` created from the `ArrayList`.
