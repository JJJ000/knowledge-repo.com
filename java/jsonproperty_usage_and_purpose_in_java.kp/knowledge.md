---
title: What is the purpose of the @jsonproperty annotation, and when is it employed?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The @JsonProperty annotation is used to specify the property name to be used when serializing and deserializing a Java object to and from JSON.
---

**Contents**

[TOC]

# Overview
The @JsonProperty annotation is used to indicate a field or method should be serialized or deserialized as a JSON property. It is a part of the Jackson JSON processor and is used to indicate that a field or method should be used as a property in the JSON representation of an object.

# Usage
The @JsonProperty annotation is used to specify the name of a property in the JSON representation of an object. This annotation can be used on either fields or getter methods. When used on a field, the annotation indicates that the field should be serialized or deserialized as a property with the specified name. When used on a getter method, the annotation indicates that the getter should be used as a property with the specified name.

# Benefits
Using the @JsonProperty annotation allows developers to control the name of the property in the JSON representation of an object. This can be useful when the field or getter name does not match the desired property name. It also allows developers to control the serialization and deserialization process, as the annotation can be used to indicate that a field or getter should be used as a property in the JSON representation of an object.

# Example
For example, if a class has a field called “name”, but the desired property name in the JSON representation is “fullName”, the @JsonProperty annotation can be used to indicate that the “name” field should be serialized and deserialized as the “fullName” property. The annotation would look like this:

@JsonProperty("fullName")
private String name;
