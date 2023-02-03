---
title: How can a user download a file that is stored in memory, without using a server?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can create a Blob object and generate a download link using the URL.createObjectURL() method.
---

**Contents**

[TOC]

## 1. Create the File

Creating the file in memory requires generating a Blob object. This can be done by passing an array of data to the Blob constructor. The data can be of any type, including strings, arrays, and even other Blob objects.

## 2. Create a URL

Once the file is created, a URL must be generated to allow the user to download it. This can be done using the URL.createObjectURL() method. This method will take the Blob object as a parameter and return a URL that can be used to access the file.

## 3. Generate a Download Link

To allow the user to download the file, a download link must be created. This can be done by creating an anchor element and setting its href attribute to the URL generated in the previous step. The download attribute can also be set to the desired filename.

## 4. Initiate the Download

Finally, the download can be initiated by calling the click() method on the anchor element. This will open a download dialog for the user to save the file.
