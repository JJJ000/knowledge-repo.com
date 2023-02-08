---
title: Transforming go structs into json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Go structs can be marshaled into JSON using the json.Marshal() function.
---

**Contents**

[TOC]

## Section 1: Go Struct

A Go struct is a collection of fields and associated data types. It is used to define a data structure that can contain different types of data. A struct is defined with the keyword `struct` followed by a list of fields surrounded by curly braces.

Example:
```go
type Person struct {
    Name string
    Age  int
}
```

## Section 2: Marshalling

Marshalling is the process of converting a Go struct into a JSON representation. This is done with the `json.Marshal()` function, which takes a Go struct as an argument and returns a JSON representation of it.

Example:
```go
person := Person{Name: "John", Age: 30}

json, err := json.Marshal(person)
if err != nil {
    panic(err)
}

fmt.Println(string(json))
```

## Section 3: JSON Output

The above code will produce the following JSON output:

```json
{"Name":"John","Age":30}
```

## Section 4: Unmarshalling

Unmarshalling is the process of converting a JSON representation back into a Go struct. This is done with the `json.Unmarshal()` function, which takes a JSON representation and a pointer to a Go struct as arguments.

Example:
```go
json := `{"Name":"John","Age":30}`

var person Person
err := json.Unmarshal([]byte(json), &person)
if err != nil {
    panic(err)
}

fmt.Println(person.Name, person.Age)
```

The above code will produce the following output:

```
John 30
```
