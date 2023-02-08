---
title: Iterating through a PHP object with changing keys
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use a foreach loop to iterate through the object and access the dynamic keys using the array syntax.
---

**Contents**

[TOC]

1. Accessing the Object:
   Before looping through the PHP Object, you must first access it. This can be done using the json_decode() function, which takes a JSON encoded string and converts it into a PHP Object.

2. Looping Through the Object:
   To loop through the PHP Object, you can use a foreach loop. This loop will iterate through each of the object's properties, allowing you to access the dynamic keys and their associated values.

3. Accessing the Dynamic Keys:
   To access the dynamic keys, you can use the object's property names. The property names are the dynamic keys, and the associated values can be accessed using the object's property values.

4. Retrieving the Values:
   Once you have accessed the dynamic keys, you can then retrieve the associated values. This can be done using the object's property values, which are the values associated with the dynamic keys.
