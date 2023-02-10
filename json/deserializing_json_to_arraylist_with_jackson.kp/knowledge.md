---
title: Convert a JSON string into an arraylist of pojos using jackson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Jackson can be used to deserialize a JSON string into an ArrayList of POJO objects.
---

**Contents**

[TOC]

**Section 1: Add Dependency to the Project**

To use Jackson to deserialize JSON to ArrayList<POJO>, you need to add the Jackson library to the project. The latest version can be downloaded from the official Jackson website.

**Section 2: Create POJO Class**

The next step is to create a POJO (Plain Old Java Object) class that will represent the data that is stored in the JSON. This class should have fields that match the data in the JSON and getter and setter methods for each field.

**Section 3: Deserialize JSON**

Once the POJO class is created, you can use the Jackson library to deserialize the JSON into an ArrayList of POJO objects. To do this, you need to create an instance of the ObjectMapper class and call the readValue() method, passing in the JSON string and the type of the ArrayList.

**Section 4: Use the ArrayList**

Once the JSON is deserialized, you can use the ArrayList of POJO objects to access the data in the JSON. For example, you can iterate over the list and access the fields of each POJO object.
