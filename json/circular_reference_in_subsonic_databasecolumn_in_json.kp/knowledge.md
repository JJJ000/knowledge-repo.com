---
title: A problem was encountered while attempting to save an object of type 'subsonic.schema.databasecolumn' due to a circular reference
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Circular references cannot be serialized in JSON.
---

**Contents**

[TOC]

**1. What is a Circular Reference?**

A circular reference is a situation where an object references itself or another object that references it in a loop. This can cause an infinite loop when the object is serialized, as the serializer will try to serialize the same object over and over again.

**2. What is Serialization?**

Serialization is the process of converting an object into a format that can be stored or transmitted. It is often used to store objects in databases or to send them over a network.

**3. What is Json?**

JSON (JavaScript Object Notation) is a data interchange format used for transferring data between systems. It is a human-readable text format with a structure similar to JavaScript objects.

**4. How to Resolve Circular Reference in Json?**

When serializing an object to JSON, circular references can be resolved by using a library such as Newtonsoft.Json, which provides an API for resolving circular references. The API can be used to replace the circular reference with a placeholder object or to ignore the circular reference entirely.
