---
title: Decode a JSON string containing a time that is not in the rfc 3339 format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: No, it is not possible to unmarshal a time that isn`t in RFC 3339 format with the encoding/json package.
---

**Contents**

[TOC]

### 1. Use a Custom Unmarshal Function

The `json.Unmarshal` function only supports RFC 3339 formatted time strings. To unmarshal a time string that isn't in RFC 3339 format, a custom unmarshal function can be used.

### 2. Define a Custom Time Type

To use a custom unmarshal function, a custom time type must be defined. This type should embed a `time.Time` type, which will be used to store the unmarshaled time.

```go
type CustomTime time.Time
```

### 3. Implement the UnmarshalJSON Function

The custom type must implement the `UnmarshalJSON` function, which will be called by `json.Unmarshal` when unmarshaling a time string. This function should parse the given time string to a `time.Time` object and store it in the `CustomTime` object.

```go
func (ct *CustomTime) UnmarshalJSON(b []byte) error {
    // Parse the time string
    t, err := time.Parse("2006-01-02", string(b))
    if err != nil {
        return err
    }

    // Store the parsed time in the CustomTime object
    *ct = CustomTime(t)
    return nil
}
```

### 4. Use the Custom Time Type

The custom time type can be used when unmarshaling a time string. The `json.Unmarshal` function will call the `UnmarshalJSON` function of the custom type, which will parse the time string and store it in the `CustomTime` object.

```go
var ct CustomTime
if err := json.Unmarshal([]byte(`"2006-01-02"`), &ct); err != nil {
    log.Fatal(err)
}
fmt.Println(ct)
```
