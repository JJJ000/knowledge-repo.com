---
title: What is the distinction between @jsonignore, @jsonbackreference, and @jsonmanagedreference?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: @JsonIgnore is used to ignore a field when serializing and deserializing an object, while @JsonBackReference and @JsonManagedReference are used to manage bidirectional relationships between objects.
---

**Contents**

[TOC]

## @JsonIgnore
@JsonIgnore is used to ignore a field or property when serializing and deserializing an object to JSON. When a field is annotated with @JsonIgnore, it will not be included in the resulting JSON.

## @JsonBackReference
@JsonBackReference is used to mark a property in a JSON object as a back reference to another object. When a field is annotated with @JsonBackReference, it will be included in the resulting JSON, but the object it refers to will not be included.

## @JsonManagedReference
@JsonManagedReference is used to mark a property in a JSON object as a managed reference to another object. When a field is annotated with @JsonManagedReference, it will be included in the resulting JSON, and the object it refers to will also be included.
