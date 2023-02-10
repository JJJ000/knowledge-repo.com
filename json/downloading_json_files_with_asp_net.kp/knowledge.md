---
title: What is the process for enabling .json file downloads using asp.net?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Set the content type of the response to `application/json` and write the JSON data to the response stream.
---

**Contents**

[TOC]

##### Setting up the Response

1. Set the `Content-Type` header of the response to `application/json`.
2. Set the `Content-Disposition` header of the response to `attachment; filename=<your-filename>.json`.

##### Writing the Content

1. Create a `StreamWriter` object with a `FileStream` object initialized with the file path of the file you want to write.
2. Write the contents of the file to the `StreamWriter` object using the `Write` method.

##### Sending the Response

1. Set the `Content-Length` header of the response to the length of the content you wrote to the file.
2. Send the response to the client.
