---
title: Process file downloads from an ajax request
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the FileSaver.js library to handle file downloads from an AJAX post in JavaScript.
---

**Contents**

[TOC]

1. Create a File Object 

To handle a file download from an ajax post, the first step is to create a file object. This can be done using the File constructor, which takes in a Blob object and an optional filename as parameters. The Blob object is the data that will be downloaded, while the filename is the name of the file that will be downloaded.

2. Create an Object URL 

The next step is to create an Object URL. This can be done using the createObjectURL() method, which takes in the file object as a parameter. This will create a unique URL that can be used to access the file object.

3. Create a Link Element 

The third step is to create a link element. This can be done using the createElement() method, which takes in the tag name of the element as a parameter. This link element should have the Object URL as its href attribute.

4. Trigger the Download 

Finally, the download can be triggered by adding the link element to the DOM and then calling the click() method on it. This will cause the browser to open a new window with the file download.
