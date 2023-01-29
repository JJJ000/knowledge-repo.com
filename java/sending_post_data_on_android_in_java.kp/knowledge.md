---
title: Submitting post information in an Android device
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the HttpURLConnection class to send POST data in Android.
---

**Contents**

[TOC]

1. Introduction

POST data is data sent from an application to a server. It is used to send information to the server, such as user input, files, or other data. In Android, POST data is sent using the HttpURLConnection class.

2. Setting up the HttpURLConnection

The first step is to create an HttpURLConnection object. This is done by using the openConnection() method of the URL class. The URL object should be initialized with the URL of the server that is being sent the POST data.

Once the HttpURLConnection object is created, it can be configured using the setRequestMethod() method. This should be set to "POST" to indicate that the data is being sent as a POST request.

3. Writing the POST Data

The next step is to write the POST data to the HttpURLConnection. This is done by using the getOutputStream() method of the HttpURLConnection class. The data should be written as a byte array.

4. Sending the POST Data

The last step is to send the POST data to the server. This is done by using the connect() method of the HttpURLConnection class. Once the data is sent, the response from the server can be read by using the getInputStream() method.
