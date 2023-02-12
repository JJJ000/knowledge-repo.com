---
title: How to modify field names using javascriptserializer.deserialize
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: You can use the `PropertyName` attribute of the JavaScriptSerializer`s Deserialize method to change field names in JSON.
---

**Contents**

[TOC]

**Section 1: Overview**
JavaScriptSerializer.Deserialize is a method used to convert a JSON string into an object. This method can be used to change the field names of a JSON object.

**Section 2: Prerequisites**
Before attempting to change the field names of a JSON object, it is important to ensure that the JSON string is valid and that the object is correctly formed. Additionally, the object should contain the correct data types for each field.

**Section 3: Process**
The process for changing the field names of a JSON object using JavaScriptSerializer.Deserialize is as follows:
1. Create a new Dictionay<string,object> variable to hold the new field names and values.
2. Use JavaScriptSerializer.Deserialize to convert the JSON string into an object.
3. Iterate through the object and add each field name and value to the new Dictionary<string,object> variable.
4. Replace the original field names with the desired field names in the new Dictionary<string,object> variable.
5. Use JavaScriptSerializer.Serialize to convert the Dictionary<string,object> variable into a JSON string.

**Section 4: Conclusion**
JavaScriptSerializer.Deserialize can be used to change the field names of a JSON object. However, it is important to ensure that the JSON string is valid and that the object contains the correct data types for each field before attempting to change the field names.
