---
title: Send an array of objects in JSON format to an ASP.NET mvc3 application
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Post the JSON data to an ASP.Net MVC3 controller action using an AJAX request.
---

**Contents**

[TOC]

#Section 1: Creating an Array of Objects

An array of objects can be created using JavaScript, JSON, or any other programming language. The objects in the array can be of any type, such as strings, numbers, booleans, objects, or arrays. Each object in the array should have a unique key that can be used to access the data within the object.

#Section 2: Posting the Array of Objects

Once the array of objects is created, it can be posted to an ASP.Net MVC3 application using the JSON format. To do this, the array of objects must be converted to a JSON string. The JSON string can then be sent to the application using an HTTP POST request.

#Section 3: Deserializing the JSON

Once the JSON string is received by the application, it must be deserialized into an array of objects. This can be accomplished using the JavaScriptSerializer class in the System.Web.Script.Serialization namespace. The DeserializeObject method can be used to convert the JSON string to an array of objects.

#Section 4: Accessing the Array of Objects

Once the array of objects has been deserialized, it can be accessed using the key of each object. The key can be used to retrieve the data from the object, which can then be used to populate a model or perform other operations.
