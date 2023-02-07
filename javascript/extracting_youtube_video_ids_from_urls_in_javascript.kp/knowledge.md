---
title: What is the youtube video id for a given url?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the string method split() to get the YouTube video ID from a URL in Javascript.
---

**Contents**

[TOC]

1.  **Extract the Video ID**
  
   The YouTube video ID is the string of characters that appears after the `v=` parameter in the URL. To extract the video ID, use the `split()` method to split the URL into an array of strings, using the `v=` parameter as the separator. Then, the video ID will be the second element in the array.

2.  **Code Example**
  
   ```javascript
   // Get the URL of the YouTube video
   let videoURL = "https://www.youtube.com/watch?v=oHg5SJYRHA0";
   
   // Split the URL at the "v=" parameter
   let videoID = videoURL.split("v=")[1];
   
   // Print the video ID
   console.log(videoID); // Output: oHg5SJYRHA0
   ```

3.  **Validate the Video ID**
  
   After extracting the video ID, it is important to validate that it is a valid YouTube video ID. To do this, you can use a regular expression to check if the video ID is of the correct format.

4.  **Code Example**
  
   ```javascript
   // Get the video ID
   let videoID = "oHg5SJYRHA0";
   
   // Use a regular expression to validate the video ID
   let isValidVideoID = /^[a-zA-Z0-9-_]{11}$/.test(videoID);
   
   // Print the result
   console.log(isValidVideoID); // Output: true
   ```
