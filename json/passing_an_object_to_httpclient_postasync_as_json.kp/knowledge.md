---
title: What is the best way to pass an object to httpclient.postasync and have it serialized as a JSON body?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Pass the object as a stringified JSON to HttpClient.PostAsync`s content parameter.
---

**Contents**

[TOC]

1. Create a JSON String
---------------------------------
Create a JSON string object that contains the data you want to send to the server. You can use a library such as Newtonsoft.Json to help with this process.

2. Set the Content-Type Header
---------------------------------
Set the content-type header of the request to application/json. This will tell the server that the request body is in JSON format.

3. Create a StringContent Object
---------------------------------
Create a StringContent object and pass it the JSON string from the first step. This will create an HttpContent object that can be passed to the PostAsync method.

4. Pass the StringContent Object to PostAsync
---------------------------------
Pass the StringContent object to the PostAsync method. This will send the JSON string to the server as the request body.
