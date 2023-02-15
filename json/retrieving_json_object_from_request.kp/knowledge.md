---
title: Getting a JSON object from an httpservletrequest
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: The JSON object literal can be retrieved from the HttpServletRequest by using the getReader() method.
---

**Contents**

[TOC]

# Section 1: Sending the JSON Object

When sending a JSON Object via an HttpServletRequest, the Object needs to be serialized into a String. This can be done using a JSON library like Jackson or Gson. The JSON String should then be added as a parameter in the request body.

# Section 2: Retrieving the JSON Object

Once the HttpServletRequest is received, the JSON Object can be retrieved using the getParameter() method. This method will return a String which can then be deserialized into a JSON Object using the same library used to serialize the Object.

# Section 3: Parsing the JSON Object

Once the JSON Object has been deserialized, it can then be parsed using the methods available in the JSON library. This will allow the user to access the properties of the Object and manipulate them as needed.

# Section 4: Returning the JSON Object

Once the Object has been manipulated, it can then be serialized back into a JSON String and returned as part of the response. This will allow the user to send the modified JSON Object back to the client.
