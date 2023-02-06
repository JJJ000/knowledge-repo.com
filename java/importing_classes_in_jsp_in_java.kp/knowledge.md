---
title: What is the process for bringing in classes in jsp?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: In JSP, classes can be imported using the `page` directive with the `import` attribute.
---

**Contents**

[TOC]

### Using the `<%@ page import %>` Directive

The `<%@ page import %>` directive is used to import classes in JSP in Java. This directive is used to import a single class or a package of classes.

### Syntax

The syntax for the `<%@ page import %>` directive is as follows:

```
<%@ page import = "package.classname" %>
```

### Example

The following example imports the `java.util.Date` class in a JSP page:

```
<%@ page import = "java.util.Date" %>
```
