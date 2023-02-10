---
title: What is the process for sending requests using JSON in unit tests?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: In unit tests for JSON, requests can be sent using an HTTP library such as Axios or Fetch.
---

**Contents**

[TOC]

1. Setup the Request

Before sending a request with JSON in unit tests, it is important to setup the request. This includes defining the request method, the URL, and any headers that need to be included. It is also important to ensure that the request is properly formatted in JSON.

2. Add the Request Body

Once the request is setup, the next step is to add the request body. This is the JSON data that will be sent in the request. Depending on the type of request, the data may need to be formatted in a specific way.

3. Execute the Request

Once the request is setup and the body is added, the next step is to execute the request. This can be done using an HTTP client library such as Axios or Superagent.

4. Assert the Response

Once the request is executed, the next step is to assert the response. This includes checking the status code, the response body, and any other relevant information. This is important to ensure that the request was successful and that the expected data was returned.
