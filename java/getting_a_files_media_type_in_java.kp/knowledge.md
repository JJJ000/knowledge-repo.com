---
title: What is the media type (mime type) of a file?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The file`s Media Type (MIME type) can be obtained in Java by using the javax.activation.MimetypesFileTypeMap class.
---

**Contents**

[TOC]

### Using the java.net.URLConnection Class
1. Create a URL object with the file path as the parameter.
2. Call the URL's `openConnection` method to get a URLConnection object.
3. Call the URLConnection's `getContentType` method to get the file's MIME type.

### Using the java.nio.Files Class
1. Create a Path object with the file path as the parameter.
2. Call the Path's `probeContentType` method to get the file's MIME type.
