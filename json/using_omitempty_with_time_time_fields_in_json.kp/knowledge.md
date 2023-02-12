---
title: Including a JSON 'omitempty' option when working with a time.time field
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Yes, the JSON `omitempty` tag can be used with time.Time fields in JSON.
---

**Contents**

[TOC]

# Section 1: Overview
When encoding a struct to JSON, the `omitempty` tag can be used to omit struct fields with empty values from the JSON output. This tag can be used with any type, including the `time.Time` type.

# Section 2: Syntax
The syntax for using the `omitempty` tag with a `time.Time` field is the same as for any other type:

```go
type MyStruct struct {
    Time time.Time `json:"time,omitempty"`
}
```

# Section 3: Example
The following example shows how to use the `omitempty` tag with a `time.Time` field:

```go
package main

import (
    "encoding/json"
    "fmt"
    "time"
)

type MyStruct struct {
    Time time.Time `json:"time,omitempty"`
}

func main() {
    myStruct := MyStruct{
        Time: time.Now(),
    }

    b, err := json.Marshal(myStruct)
    if err != nil {
        fmt.Println(err)
        return
    }

    fmt.Println(string(b))
}
```

# Section 4: Output
The above example will output the following JSON:

```json
{"time":"2020-08-17T15:30:00Z"}
```
