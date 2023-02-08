---
title: The correct method for sending back JSON data using Node.js or express.js
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The proper way to return JSON using node or Express is to use the res.json() function.
---

**Contents**

[TOC]

# Section 1: Setting Up the Response

When returning JSON using node or Express, the first step is to set up the response. This is done by using the `res.setHeader()` method. This method takes two parameters: the name of the header and the value of the header. In this case, the header name should be `Content-Type` and the value should be `application/json`.

# Section 2: Writing the JSON

The next step is to write the JSON. This can be done by using the `res.write()` method. This method takes a single parameter, which should be a valid JSON string.

# Section 3: Sending the Response

Once the JSON is written, the response can be sent using the `res.end()` method. This method takes no parameters and simply sends the response.

# Section 4: Handling Errors

Finally, it is important to handle any errors that may occur. This can be done by using the `res.on('error', callback)` method. This method takes a single parameter, which should be a callback function. This callback function will be called if an error occurs and can be used to handle the error appropriately.
