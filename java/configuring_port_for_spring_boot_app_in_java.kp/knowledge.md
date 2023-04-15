---
title: What are the steps to set up a port for a spring boot application?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Configure the port for a Spring Boot application in Java by setting the server.port property in the application.properties file.
---

**Contents**

[TOC]

### Configure Server Port

1. Open the `application.properties` file in the `src/main/resources` folder.
2. Add the following line to the file: `server.port=<port_number>`. 
3. Replace `<port_number>` with the desired port number.
4. Save the file.

### Configure JVM

1. Open the `application.yml` file in the `src/main/resources` folder.
2. Add the following line to the file: `server.port: <port_number>`. 
3. Replace `<port_number>` with the desired port number.
4. Save the file.

### Command Line Arguments

1. Open the `application.yml` file in the `src/main/resources` folder.
2. Add the following line to the file: `--server.port=<port_number>`. 
3. Replace `<port_number>` with the desired port number.
4. Save the file.

### Environment Variables

1. Open the `application.yml` file in the `src/main/resources` folder.
2. Add the following line to the file: `SERVER_PORT=<port_number>`. 
3. Replace `<port_number>` with the desired port number.
4. Save the file.
