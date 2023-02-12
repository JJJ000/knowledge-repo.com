---
title: Retrieve a JSON object from the http body using an mvc controller
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: The controller can use the HttpRequest object to get the JSON object from the HTTP body.
---

**Contents**

[TOC]

**Section 1: Retrieve the JSON Object**

The first step is to retrieve the JSON object from the HTTP body. This can be done using the `request.getBody()` method. This method will return the body of the request as a string.

**Section 2: Convert String to JSON Object**

Once the JSON object has been retrieved, the next step is to convert the string into a JSON object. This can be done using the `JSON.parse()` method. This method will parse the string into a JSON object, allowing it to be manipulated as needed.

**Section 3: Access the JSON Object**

Once the JSON object has been created, it can then be accessed and manipulated as needed. This can be done using the `JSON.get()` method. This method will allow the program to access the data within the JSON object.

**Section 4: Manipulate the JSON Object**

Finally, the program can manipulate the JSON object as needed. This can be done using the `JSON.set()` method. This method will allow the program to set values within the JSON object. It can also be used to update existing values in the object.
