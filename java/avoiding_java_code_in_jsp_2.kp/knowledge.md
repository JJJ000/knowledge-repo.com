---
title: What is the best way to prevent the use of Java code in JSP files when using JSP 2?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: Use tag files and custom tags instead of Java code in JSP files.
---

**Contents**

[TOC]

### Use the JSP Expression Language (EL)

The JSP Expression Language (EL) allows developers to access data stored in JavaBeans components, as well as other objects like request, session, and application-scoped variables. EL provides a simplified way to access data without having to write Java code.

### Use JSTL and Custom Tags

JSP Standard Tag Library (JSTL) is a collection of custom tags that can be used to simplify the development of JSP pages. JSTL tags provide a declarative approach to accessing data and performing operations on the data. Custom tags can also be used to encapsulate complex operations and reduce the amount of Java code required in a JSP page.

### Use Include Directive

The include directive can be used to include content from another source into a JSP page. This allows developers to separate the Java code from the JSP page and keep the code in separate files. This helps to keep the code organized and makes it easier to maintain.

### Use MVC Frameworks

Using an MVC framework like Spring or Struts can help to reduce the amount of Java code in JSP pages. These frameworks provide a way to separate the presentation layer from the business logic, which helps to keep the code organized and easier to maintain.
