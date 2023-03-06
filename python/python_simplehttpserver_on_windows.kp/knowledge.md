---
title: How to install simplehttpserver on windows using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To set up Python simpleHTTPserver on Windows, open command prompt or terminal and type `python -m http.server` and hit enter.
---

**Contents**

[TOC]

## Prerequisite

Before setting up the Python simpleHTTPserver on Windows, make sure Python is installed on your computer. If you do not have it installed, go to the Python download page and install it.


## Steps to Set up Python simpleHTTPserver

1. Open the command prompt or terminal window in your computer.
2. Navigate to the folder where you want to set up the SimpleHTTPServer.
3. Type Python -m http.server in the command prompt or terminal window.
4. Hit enter and then wait for the http.server to start.

Once it’s started, you can navigate to http://localhost:8000 in your web browser, and you should see the files and folders in your folder that you pointed the server to.

This server will automatically update when you add, remove or edit any files in your folder.

## Other considerations

By default, SimpleHTTPServer runs on port 8000. If you want to run it on a different port, specify it as an argument when starting the server, like so: 

```
Python -m http.server 8080
```
 
This will run the server on port 8080.


Make sure to stop the server with `ctrl+c` once you are done using it.
