---
title: When running in detached mode within docker, the Python application fails to display any output
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Detached mode in Docker suppresses the standard output, so print statements in the Python app are not visible.
---

**Contents**

[TOC]

Problem Description
-------------------
A Python app running inside a Docker container does not print anything when the container is run in detached mode.


Possible Solutions
-------------------
1. Use logging instead of print:
   
   A better way to debug and troubleshoot a Python app running inside a container is to use the `logging` library instead of print statements. This provides more control over the output and can be directed to different destinations (such as files, syslog, or remote log collectors). Updating the app to use `logging` instead of print statements can be a more reliable long-term solution.

2. Check container logs:

   In detached mode, Docker containers run in the background, which makes it difficult to see the application output. This is where `docker logs` command comes to rescue. To view the output of a detached container, use `docker logs <container_name>` command. This will print the output of the app to the stdout of the container. 

3. Use docker-compose:

   Another way to run a container in detached mode and still be able to view the output is to use `docker-compose` instead of `docker` command. By using `docker-compose`, we can specify the service logs in either the foreground or background. The following command runs the container in detached mode but allows us to view the output using `docker-compose logs`:

   ```
   version: '3'
   
   services:
     myapp:
       image: myapp:latest
       command: python app.py 
       stdin_open: true
       tty: true
       logging:
         driver: "json-file"
         options:
           max-size: "10m"
           max-file: "3"
   ```

4. Check application code:

   The issue could also be with the application code itself. It is possible that the part of the application that was supposed to print output might not be run in the detached mode in the docker container. It is important to make sure that the parts of the application that needs to print output are run with debugging output options enabled. 

Conclusion
----------
There can be several reasons why a Python app running inside a Docker container does not print anything when running detached. The problem could be with application code or an issue with the way the container is being run. Using `logging` instead of print statements is a better and much more reliable way to debug such issues in the long run. Otherwise, using the `docker logs`  or `docker-compose` commands can help us view the application output in detached mode.
