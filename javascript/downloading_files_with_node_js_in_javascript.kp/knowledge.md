---
title: What is the process for downloading a file using Node.js without external libraries?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Using the built-in http module, you can make a request to a file URL and pipe the response directly to a file stream.
---

**Contents**

[TOC]

### Section 1: Setup

Before downloading the file, you will need to set up the environment to make sure that the download process goes smoothly. 

1. Create a directory to store the file and set up the necessary permissions. 
2. Install the necessary dependencies, such as the `fs` module.
3. Set up a `http` or `https` request to the file's URL.

### Section 2: Request File

Once you have set up the environment, you can now make a request for the file.

1. Create a `http` or `https` request to the file's URL.
2. Check the response status code to ensure that the request was successful.
3. If the request was successful, read the response body and store it in a variable.

### Section 3: Write File

Once the file has been requested and stored in a variable, you can now write it to the directory you created earlier.

1. Use the `fs` module to write the file to the directory.
2. Check the response status code to ensure that the file has been written successfully.

### Section 4: Cleanup

Once the file has been successfully written to the directory, you can now clean up the environment.

1. Close the `http` or `https` request.
2. Delete the variable containing the file data.
3. Delete any unnecessary files or directories.
