---
title: What is the best way to avoid marshaling an empty struct into JSON with go?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the `omitempty` tag when marshalling the struct into JSON.
---

**Contents**

[TOC]

### Section 1 - Prerequisites

Before attempting to not marshal an empty struct into JSON, it is important to understand the basics of the Go programming language and the JSON data interchange format.

### Section 2 - Use Struct Tags

Struct tags can be used to prevent an empty struct from being marshaled into JSON. Struct tags are key-value pairs that are associated with a struct field. To prevent an empty struct from being marshaled, you can add a `omitempty` tag to the struct field. This will prevent the struct field from being marshaled into JSON if it is empty.

### Section 3 - Use Custom Marshaling

You can also use custom marshaling to prevent an empty struct from being marshaled into JSON. Custom marshaling allows you to define custom logic for marshaling a struct into JSON. This can be used to check if a struct field is empty and, if it is, not marshal it into JSON.

### Section 4 - Conclusion

By using struct tags or custom marshaling, you can prevent an empty struct from being marshaled into JSON with Go. Struct tags are the simpler of the two options, but custom marshaling can provide more control over how a struct is marshaled into JSON.
