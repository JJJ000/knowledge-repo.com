---
title: Transform a JSON array into a regular Java list
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the Gson library to parse the JSON array into a List of Java objects.
---

**Contents**

[TOC]

##### Step 1: Create a Java class to represent the JSON array

Create a Java class to represent the JSON array. This class should contain fields for each element in the array.

##### Step 2: Parse the JSON array

Parse the JSON array into an instance of the Java class created in Step 1. This can be done using a JSON library such as Gson.

##### Step 3: Create a list

Create a normal Java list (e.g. `List<MyClass>`) and add the instances of the Java class created in Step 2 to the list.

##### Step 4: Iterate over the list

Iterate over the list and access the elements as needed.
