---
title: What is the best way to format JSON using go?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can pretty-print JSON using Go by using the `encoding/json` package`s MarshalIndent() function.
---

**Contents**

[TOC]

## Section 1: Using the Standard Library
Go provides a `json` package in its standard library that can be used for pretty-printing JSON. The package provides a `MarshalIndent` function that takes a Go data structure and converts it to a JSON string, with indentation for readability.

## Section 2: Example
Below is an example of using `MarshalIndent` to pretty-print a simple Go struct:

```go
type Person struct {
    Name string
    Age  int
}

person := Person{
    Name: "John Doe",
    Age:  42,
}

jsonBytes, err := json.MarshalIndent(person, "", "  ")
if err != nil {
    log.Fatalf("Error marshaling JSON: %s", err)
}

fmt.Println(string(jsonBytes))
```

The output of the above code would be:

```json
{
  "Name": "John Doe",
  "Age": 42
}
```

## Section 3: Options
The `MarshalIndent` function takes two parameters that control the formatting of the output JSON. The first parameter is a prefix string that will be added to the beginning of each line of the output. The second parameter is a string that will be used for indentation.

## Section 4: Further Reading
For more information on the `json` package, see the [documentation](https://golang.org/pkg/encoding/json/).
