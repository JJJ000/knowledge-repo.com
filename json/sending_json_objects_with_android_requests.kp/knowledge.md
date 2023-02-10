---
title: What is the best way to send a JSON object using an Android request?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Send the JSON object as a StringEntity in the request body.
---

**Contents**

[TOC]

# Section 1: Setting up the Request

1. Create a new `HttpURLConnection` object, passing in the URL to which you are sending the request.
2. Set the request method to `POST` and set the request body content type to `application/json`.
3. Set the request headers to `Content-Type: application/json` and `Accept: application/json`.

# Section 2: Creating the JSON Object

1. Create a new `JSONObject` object.
2. Add key-value pairs to the object.
3. Use the `put` method to add a key-value pair to the object.

# Section 3: Writing the Request Body

1. Create a `StringWriter` object.
2. Create a `JSONWriter` object, passing in the `StringWriter` object.
3. Use the `writeObject` method of the `JSONWriter` object to write the `JSONObject` to the request body.

# Section 4: Sending the Request

1. Get the request body as a `String` by calling the `toString` method of the `StringWriter` object.
2. Get the `OutputStream` from the `HttpURLConnection` object.
3. Write the request body `String` to the `OutputStream`.
4. Close the `OutputStream`.
5. Send the request by calling the `connect` method of the `HttpURLConnection` object.
