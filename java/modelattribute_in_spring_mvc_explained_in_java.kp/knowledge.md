---
title: How does @modelattribute work in spring mvc?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: @ModelAttribute is an annotation used in Spring MVC to bind method parameters or fields to objects in the model.
---

**Contents**

[TOC]

### Overview

@ModelAttribute is an annotation used in Spring MVC. It is used to bind data from the request (query parameters, form data, etc.) to a model object. This annotation can be used on a method argument, a method return value, or a class field.

### Binding Data to Model Object

When the @ModelAttribute annotation is used on a method argument, the parameter is populated with data from the request. This data can be retrieved from the query parameters, form data, or other sources. The data is then bound to the model object, and the model object is passed into the method.

### Binding Data to Model Object

When the @ModelAttribute annotation is used on a method return value, the model object is populated with data from the request. This data can be retrieved from the query parameters, form data, or other sources. The data is then bound to the model object, and the model object is returned from the method.

### Class Field

When the @ModelAttribute annotation is used on a class field, the field is populated with data from the request. This data can be retrieved from the query parameters, form data, or other sources. The data is then bound to the field, and the field is available to be used in the class.
