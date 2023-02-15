---
title: Returning a JSON payload and http status code in a flask response
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Flask provides the jsonify() function to easily create a response with JSON data and a specific status code.
---

**Contents**

[TOC]

# Section 1: Setting Up the Flask Response

To send a JSON response with a status code in Flask, you need to use the `make_response` method. This method takes two arguments, the response body and the status code.

# Section 2: Constructing the Response Body

The response body should be a Python dictionary that can be converted to a JSON object. This can be done using the `jsonify` method from the Flask `json` library.

# Section 3: Setting the Status Code

The status code can be set using the `make_response` method. This method takes an optional argument for the status code.

# Section 4: Sending the Response

Once the response body and status code have been set, the response can be sent using the `make_response` method. This method returns a response object which can be sent using the `return` statement.
