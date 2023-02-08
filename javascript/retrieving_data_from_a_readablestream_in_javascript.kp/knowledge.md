---
title: Fetch information from a readablestream object?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Data can be retrieved from a ReadableStream object by calling the ReadableStream.getReader() method and using the reader`s read() method.
---

**Contents**

[TOC]

### Readable Stream
A ReadableStream object is a JavaScript object that allows you to read data from a source such as a file, a network request, or a text string. The data can be read as chunks, which are pieces of data that are read from the source and then processed by the user.

### Retrieving Data
The ReadableStream object provides a number of methods for retrieving data from the source. The most common methods are `read()` and `pipe()`.

`read()` is used to read a single chunk of data from the source. It returns a Promise that resolves with the data when it is available.

`pipe()` is used to pipe data from the source to a destination. It takes two arguments, a source and a destination, and will read data from the source and write it to the destination as it becomes available.

### Processing Data
Once the data has been retrieved from the source, it can be processed by the user. This can be done using the `on('data')` event handler, which is triggered whenever a new chunk of data is available. The data can then be processed and used as needed.

### Error Handling
If an error occurs while retrieving or processing data from the source, the `on('error')` event handler can be used to handle the error. This event handler will be triggered whenever an error occurs and will provide information about the error that occurred.
