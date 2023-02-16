---
title: How to exclude empty nested structures when using the go programming language's JSON marshalling feature
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: Use the `omitempty` tag on the fields of the nested struct to omit them when marshaling.
---

**Contents**

[TOC]

1. Overview
When using the Go language's `json.Marshal` function, it is possible to omit empty nested structs in the outputted JSON. This can be accomplished by implementing a custom marshaler and setting the `omitempty` tag on the struct field.

2. Implementing a Custom Marshaler
In order to omit empty nested structs, a custom marshaler must be implemented. This is done by creating a type which implements the `json.Marshaler` interface and defining a `MarshalJSON` method for it.

3. Setting the `omitempty` Tag
The `omitempty` tag can then be set on the struct field. This tag will cause the field to be omitted from the outputted JSON if it is empty.

4. Example
Here is an example of how to omit empty nested structs using a custom marshaler and the `omitempty` tag.

```go
type MyStruct struct {
    Field1 string
    Field2 NestedStruct `json:"nested,omitempty"`
}

type NestedStruct struct {
    Field1 int
    Field2 string
}

func (s MyStruct) MarshalJSON() ([]byte, error) {
    type Alias MyStruct
    return json.Marshal(&struct {
        Alias
    }{
        Alias: (Alias)(s),
    })
}
```
