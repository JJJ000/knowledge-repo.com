---
title: Transform go map into JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can convert a Go map to JSON by using the json.Marshal() function.
---

**Contents**

[TOC]

# Section 1: Overview

Go maps can be converted to JSON using the built-in encoding/json package. This package provides the Marshal and Unmarshal functions, which can be used to convert a Go map to JSON and vice versa.

# Section 2: Encoding a Go Map to JSON

The encoding/json package provides the Marshal function to convert a Go map to JSON. The Marshal function takes a Go map as an argument and returns a JSON-encoded byte array. The following example shows how to use the Marshal function to convert a Go map to JSON:

```go
package main

import (
	"encoding/json"
	"fmt"
)

func main() {
	// Create a Go map
	myMap := map[string]string{
		"foo": "bar",
		"baz": "qux",
	}

	// Convert the Go map to JSON
	jsonBytes, err := json.Marshal(myMap)
	if err != nil {
		panic(err)
	}

	// Print the JSON-encoded byte array
	fmt.Println(string(jsonBytes))
}
```

# Section 3: Decoding a JSON String to a Go Map

The encoding/json package also provides the Unmarshal function to convert a JSON string to a Go map. The Unmarshal function takes a JSON-encoded byte array and a Go map as arguments and returns an error if it fails. The following example shows how to use the Unmarshal function to convert a JSON string to a Go map:

```go
package main

import (
	"encoding/json"
	"fmt"
)

func main() {
	// Create a JSON string
	jsonStr := `{"foo": "bar", "baz": "qux"}`

	// Create a Go map
	myMap := make(map[string]string)

	// Convert the JSON string to the Go map
	err := json.Unmarshal([]byte(jsonStr), &myMap)
	if err != nil {
		panic(err)
	}

	// Print the Go map
	fmt.Println(myMap)
}
```

# Section 4: Conclusion

In conclusion, the encoding/json package provides the Marshal and Unmarshal functions to convert a Go map to JSON and vice versa. This can be useful when working with APIs that require data to be in JSON format.
