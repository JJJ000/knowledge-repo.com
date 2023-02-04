---
title: What steps can I take to resolve the error listen eaddrinuse when using nodejs?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The error can be fixed by changing the port number being used by the NodeJS server.
---

**Contents**

[TOC]

## Step 1: Identify the Port Number
The first step in resolving the error is to identify the port number that is already in use. 

## Step 2: Find the Process Listening on the Port
Once the port number is identified, the next step is to find the process that is already listening on the port. This can be done by running the command `netstat -ano | findstr <port_number>` in the command line. 

## Step 3: Stop the Process
Once the process is identified, it can be stopped by running the command `taskkill /F /PID <process_id>`. 

## Step 4: Retry the Node.js Server
Finally, the Node.js server can be retried to check if the error has been resolved.
