---
title: What is the process for converting JSON to a c# object?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can deserialize JSON with C# using the JsonSerializer class.
---

**Contents**

[TOC]

**Section 1 - Install Newtonsoft.Json**

The first step to deserializing JSON with C# is to install the Newtonsoft.Json NuGet package. This package provides a library of classes and methods that can be used to serialize and deserialize JSON.

**Section 2 - Create a Model Class**

The next step is to create a model class that matches the structure of the JSON data. This model class will be used to store the deserialized data.

**Section 3 - Deserialize the JSON Data**

Once the model class has been created, the JSON data can be deserialized into an object of the model class. This can be done using the JsonConvert.DeserializeObject method from the Newtonsoft.Json library.

**Section 4 - Access the Deserialized Data**

Once the JSON data has been deserialized, the data can be accessed using the properties of the model class. For example, if the JSON data contains a list of objects, the list can be accessed using the model class's List property.
