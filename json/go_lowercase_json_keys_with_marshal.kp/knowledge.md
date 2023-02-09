---
title: Use JSON marshal in go to convert lowercase key names in json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: JSON Marshal in Go will automatically convert all keys to lowercase when marshaling a struct into JSON.
---

**Contents**

[TOC]

# Using JSON Marshal

JSON Marshal is an encoding/json package in Go that allows for the conversion of Go objects into JSON strings. It is a great tool for converting structs into JSON objects, which can then be used in web applications.

## Lowercase JSON Keys

By default, JSON Marshal will convert struct fields into JSON keys with the same name as the struct field, but with the first letter capitalized. To convert the JSON keys to lowercase, we can use the `json:"fieldname"` tag on the struct field.

For example, if we have a struct like this:

```go
type Person struct {
    Name string
    Age int
}
```

We can convert it to JSON with JSON Marshal like this:

```go
person := Person{
    Name: "John Doe",
    Age: 42,
}

jsonBytes, err := json.Marshal(person)
if err != nil {
    log.Fatalf("error marshalling person: %v", err)
}
fmt.Println(string(jsonBytes))
```

This will output the following JSON:

```json
{"Name":"John Doe","Age":42}
```

## Lowercase JSON Keys with Tags

If we want to convert the JSON keys to lowercase, we can add the `json:"fieldname"` tag to the struct fields, like this:

```go
type Person struct {
    Name string `json:"name"`
    Age int `json:"age"`
}
```

Now, when we marshal the struct into JSON, the keys will be lowercase:

```json
{"name":"John Doe","age":42}
```
