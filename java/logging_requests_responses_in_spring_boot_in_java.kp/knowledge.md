---
title: How can I log all requests, responses, and exceptions for spring boot in one location?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use a Filter to log all requests and responses with exceptions in a single place in a Spring Boot application.
---

**Contents**

[TOC]

1. Overview 
2. Configure Logback Appender 
3. Create Custom Logging Filter 
4. Configure Spring Boot Logging

### 1. Overview 
Logging all requests and responses with exceptions in a single place is an important part of any application. It provides insight into the performance and behaviour of the application and helps in debugging any issues. In Java, this can be achieved by configuring a logback appender, creating a custom logging filter, and configuring Spring Boot logging. 

### 2. Configure Logback Appender 
Logback is the default logging framework used in Spring Boot. To configure a logback appender, create a logback-spring.xml file in the src/main/resources folder and add the following configuration: 

```java
<?xml version="1.0" encoding="UTF-8"?>
<configuration>
    <appender name="REQUESTS" class="ch.qos.logback.core.FileAppender">
        <file>requests.log</file>
        <encoder>
            <pattern>%d{HH:mm:ss.SSS} [%thread] %-5level %logger{36} - %msg%n</pattern>
        </encoder>
    </appender>
    <appender name="RESPONSES" class="ch.qos.logback.core.FileAppender">
        <file>responses.log</file>
        <encoder>
            <pattern>%d{HH:mm:ss.SSS} [%thread] %-5level %logger{36} - %msg%n</pattern>
        </encoder>
    </appender>
    <appender name="EXCEPTIONS" class="ch.qos.logback.core.FileAppender">
        <file>exceptions.log</file>
        <encoder>
            <pattern>%d{HH:mm:ss.SSS} [%thread] %-5level %logger{36} - %msg%n</pattern>
        </encoder>
    </appender>
    <logger name="org.springframework.web" level="DEBUG" additivity="false">
        <appender-ref ref="REQUESTS"/>
        <appender-ref ref="RESPONSES"/>
        <appender-ref ref="EXCEPTIONS"/>
    </logger>
</configuration>
```

This configuration will create three log files - requests.log, responses.log, and exceptions.log. The logback appender will log all requests, responses, and exceptions in the respective log files. 

### 3. Create Custom Logging Filter 
To log all requests and responses in a single place, create a custom logging filter. The filter should be configured to log requests and responses in a single log file. To create a custom logging filter, create a class that implements the javax.servlet.Filter interface. This class should override the doFilter() method and add the necessary logic to log requests and responses. 

### 4. Configure Spring Boot Logging 
Finally, configure Spring Boot logging to use the custom logging filter. To do this, add the following configuration to the application.properties file: 

```java
logging.filter.type=<custom_filter_class_name>
```

This will configure Spring Boot to use the custom logging filter for all requests and responses.
