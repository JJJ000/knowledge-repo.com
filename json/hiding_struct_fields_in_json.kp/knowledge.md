---
title: Eliminating elements from a struct or concealing them in a JSON response
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can remove fields from a struct by using the `omitempty` tag, or hide them in a JSON response by using an anonymous struct.
---

**Contents**

[TOC]

## Removing Fields from Struct

Removing fields from a struct can be done by simply deleting the field from the struct, either manually or using the `delete` keyword. For example, to remove a field called `name` from a struct called `Person`:

```go
type Person struct {
    Name string
    Age  int
}

// To delete the Name field:
delete(Person, "Name")
```

## Hiding Fields in JSON Response

Hiding fields in a JSON response can be done by using the `omitempty` tag on the field in the struct. This tag tells the JSON encoder to ignore the field when it is empty. For example, to hide a field called `name` from a JSON response when it is empty:

```go
type Person struct {
    Name string `json:"name,omitempty"`
    Age  int
}
```

This will cause the JSON encoder to omit the `name` field from the response when it is empty.
