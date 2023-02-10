---
title: Convert a string to a float64 by decoding it from json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the json.Unmarshal() function with a custom type that contains the desired type (float64) for the desired field.
---

**Contents**

[TOC]

# Section 1: Preparation
Before attempting to decode a JSON string with type conversion from string to float64, it is important to ensure that the JSON string is valid and properly formatted. This can be done using a JSON validator such as JSONLint. If the JSON string is valid, the next step is to determine the data type of the value that needs to be converted from string to float64.

# Section 2: Decoding the JSON String
Once the JSON string is valid and the data type of the value to be converted is known, the next step is to decode the string. This can be done using a JSON decoder library such as json.decode. The decoder will return a data structure, such as a map or struct, which can then be used to access the value to be converted.

# Section 3: Converting the Value
Once the value to be converted is accessed, it can then be converted from a string to a float64 using the strconv.ParseFloat function. This function takes a string and a bit size as arguments and returns a float64.

# Section 4: Testing the Conversion
Once the value has been converted, it is important to test it to ensure that the conversion was successful. This can be done by comparing the original value to the converted value. If the values are the same, then the conversion was successful. If not, then the conversion was not successful and should be reattempted.
