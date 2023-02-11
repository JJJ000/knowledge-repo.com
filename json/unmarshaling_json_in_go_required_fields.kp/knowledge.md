---
title: What is needed to successfully unmarshal JSON in go?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: No, there are no required fields when unmarshaling JSON in Go.
---

**Contents**

[TOC]

## Unmarshal

The `Unmarshal` function in Go is used to convert a JSON string into a data structure. This function takes a JSON string and a pointer to a data structure as its arguments. The data structure must be a valid Go type, such as a struct, an array, a map, etc.

## Required Fields

When unmarshaling a JSON string, it is possible to specify which fields are required. This is done by setting the `omitempty` tag on the struct field. If the JSON string does not contain a value for the field marked with `omitempty`, the `Unmarshal` function will return an error.

## Example

For example, if we have the following struct:

```go
type Person struct {
    Name string `json:"name,omitempty"`
    Age  int    `json:"age"`
}
```

The `Name` field is marked with the `omitempty` tag, so if the JSON string does not contain a value for the `name` field, the `Unmarshal` function will return an error.

## Conclusion

In conclusion, the `Unmarshal` function in Go can be used to convert a JSON string into a data structure, and it is possible to specify which fields are required by setting the `omitempty` tag on the struct field.
