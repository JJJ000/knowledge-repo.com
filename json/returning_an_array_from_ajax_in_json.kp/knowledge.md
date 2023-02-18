---
title: What is the process for retrieving an array from an ajax call?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: The AJAX call can return an array by encoding it as JSON and setting the response type to `application/json`.
---

**Contents**

[TOC]

1. Prepare the Data #

Before returning an array from an AJAX call, the data must first be prepared. This means that the data must be formatted in a way that is compatible with JSON. This can be done by using a library such as JSON.stringify() which will convert the data into a valid JSON string.

2. Set the Response Type #

The response type must be set to JSON in order for the AJAX call to recognize the data as a valid JSON array. This can be done by setting the responseType property of the AJAX call to "JSON".

3. Return the Data #

Once the data has been prepared and the response type has been set, the data can be returned from the AJAX call. This can be done by using the return statement and passing in the JSON stringified data.

4. Parse the Data #

Finally, the data must be parsed in order to access the array elements. This can be done by using a library such as JSON.parse() which will convert the JSON string into an array of objects.
