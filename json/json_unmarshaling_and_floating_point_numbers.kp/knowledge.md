---
title: When you attempt to unmarshal JSON data with long numbers, the result is presented as a floating point number
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: This happens because JSON does not have a specific data type for long integers and defaults to using floating-point numbers.
---

**Contents**

[TOC]

Overview:

JSON unmarshaling is the process of converting data stored in JSON format to a Go data structure. This is typically done using the standard library `encoding/json` package. However, when working with long numbers, there is the possibility that the resulting Go data structure may not accurately represent the original JSON data. In particular, the use of floating point numbers to represent long integers can cause issues. This article will explore the reasons behind this issue and suggest ways to avoid it when working with JSON data in Go.

Section 1: Introduction to JSON unmarshaling

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is easy for humans to read and write and easy for machines to parse and generate. This format is widely used to transmit data between client and server in web applications. In Go, the `encoding/json` package is used to work with JSON data.

Unmarshaling is the process of mapping JSON data to a Go data structure. The `encoding/json` package provides the `Unmarshal` function, which takes a byte slice containing JSON data and a pointer to a Go data structure. The function then populates the Go data structure with the corresponding data from the JSON data.

Section 2: JSON Numbers

In JSON, numbers may be either integers or floating-point numbers. In Go, the standard library has separate types `int` and `float64` to represent these two types of numbers. However, the Go `json` package treats all JSON numbers as `float64` by default when unmarshaling JSON data.

While 64-bit floating point numbers (float64) can represent a wide range of values, they cannot represent all integer values with perfect accuracy. This means that when an integer value is unmarshaled from JSON and stored in a float64 variable, the resulting value may not be exactly equal to the original integer.

Section 3: JSON long numbers and floating point approximation

When working with long integers in JSON, the use of floating point approximations can lead to problems. This is because long integers may require more than 53 bits of precision, which is the maximum number of bits that can be accurately represented by a float64. When an integer value that requires more than 53 bits is unmarshaled from JSON, it will be approximated as a floating point number.

For example, consider the following JSON data:

    {
        "value": 9007199254740993
    }

This is a simple JSON object with a single key, `value`, whose value is the integer 9007199254740993. If we attempt to unmarshal this data into a Go struct, we might use the following code:

    type MyData struct {
        Value int64 `json:"value"`
    }

    myData := MyData{}

    data := []byte(`{
        "value": 9007199254740993
    }`)

    json.Unmarshal(data, &myData)

However, when we print the value of `myData.Value`, we get:

    fmt.Println(myData.Value) // output: 9.007199254740993e+15

This output shows that the integer value we attempted to unmarshal into `myData.Value` has been approximated as a floating point number. This approximation can lead to loss of precision when performing calculations on the number, which can cause errors in our program.

Section 4: Best practices to avoid JSON floating point number

To avoid loss of precision when working with long integers in JSON data, we can use string values instead of numerical values for these integers. This means that we will need to modify our Go struct to use a different type to store the integer value:

    type MyData struct {
        Value json.Number `json:"value"`
    }

    myData := MyData{}

    data := []byte(`{
        "value": "9007199254740993"
    }`)

    json.Unmarshal(data, &myData)

In this modified version of our struct, we are using the `json.Number` type to represent the integer value. This type is provided by the `encoding/json` package and is used to store numbers that do not fit into standard Go data types.

By choosing to store the integer value as a string in our JSON data, we can avoid the approximation of long integers as floating point numbers when unmarshaling the data. This allows us to preserve the full precision of the original integer value, ensuring that our program performs as expected.

Conclusion

JSON unmarshaling is an important process in working with web applications. However, when dealing with long integers, we must be careful to avoid the approximation of these integers as floating point numbers. By choosing to store these integers as strings in our JSON data and using the `json.Number` type to represent them in Go, we can preserve the full precision of the original integer values and avoid errors in our program.
