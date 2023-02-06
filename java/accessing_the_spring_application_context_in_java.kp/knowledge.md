---
title: Retrieving the spring application context
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The Spring ApplicationContext can be obtained by calling the static method `getApplicationContext()` on the org.springframework.context.ApplicationContext class.
---

**Contents**

[TOC]

# Section 1: Overview

Spring Application Context is a lightweight container that provides the necessary infrastructure for an application to run. It is responsible for managing the lifecycle of beans and their dependencies. It also provides support for internationalization, event-handling, and resource management.

# Section 2: Getting the Application Context

The ApplicationContext can be obtained by either instantiating it directly or by using the Spring Framework's ApplicationContextAware interface. To instantiate the ApplicationContext, the following code can be used:

```
ApplicationContext context = new AnnotationConfigApplicationContext(MyConfiguration.class);
```

To use the ApplicationContextAware interface, the following code can be used:

```
public class MyBean implements ApplicationContextAware {
 
    private ApplicationContext context;
 
    public void setApplicationContext(ApplicationContext context) {
        this.context = context;
    }
}
```

# Section 3: Accessing Beans

Once the ApplicationContext has been obtained, the beans that it contains can be accessed using the getBean() method. This method takes a single argument which is the name of the bean to be retrieved. For example, the following code will retrieve the bean with the name "myBean":

```
MyBean myBean = (MyBean) context.getBean("myBean");
```

# Section 4: Closing the Application Context

When the application is finished, the ApplicationContext should be closed to free up any resources that it is using. This can be done using the close() method. For example:

```
context.close();
```
