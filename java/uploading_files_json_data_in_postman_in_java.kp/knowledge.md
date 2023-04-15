---
title: What is the process for sending a file and JSON data using postman?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Java, a file and JSON data can be uploaded to Postman using the Postman API`s `sendMultipartFormData` method.
---

**Contents**

[TOC]

### Setting Up Postman

1. Download and install Postman from the official website.
2. Launch Postman and create a new request.
3. Select the type of request you would like to make, such as a POST request.
4. Enter the URL of the API endpoint you would like to send the request to.

### Uploading the File

1. Select the “Body” tab in Postman.
2. Select “form-data” from the drop-down menu.
3. Enter the name of the file you would like to upload in the “key” field.
4. Select “File” from the drop-down menu.
5. Click “Choose Files” and select the file you would like to upload.
6. Click “Send” to upload the file.

### Uploading the JSON Data

1. Select the “Body” tab in Postman.
2. Select “raw” from the drop-down menu.
3. Select “JSON” from the drop-down menu.
4. Enter the JSON data you would like to send in the text box.
5. Click “Send” to upload the JSON data.

### Verifying the Upload

1. Check the response from the API to verify that the upload was successful.
2. If the response is successful, the file and JSON data should be uploaded successfully.
