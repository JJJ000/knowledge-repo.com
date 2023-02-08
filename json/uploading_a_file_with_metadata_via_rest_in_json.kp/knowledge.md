---
title: What is the process for sending a file with associated data to a rest web service?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Send a POST request to the web service endpoint with the file data and the desired metadata included in the request body as a JSON object.
---

**Contents**

[TOC]

1. Create the JSON Request
----------------------------
The JSON request should include the metadata for the file being uploaded as well as the file itself. The file should be encoded in base64.

2. Send the Request
-------------------
The request should be sent to the REST web service using an HTTP POST request.

3. Handle the Response
----------------------
The response from the web service should indicate if the file was successfully uploaded. If the response indicates success, the file should be available on the server.

4. Verify the File
------------------
The file should be verified to ensure that it was uploaded correctly. This can be done by comparing the file's metadata with the metadata included in the original request.
