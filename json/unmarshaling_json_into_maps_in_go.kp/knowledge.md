---
title: Unmarshal part of a JSON string into a map in go
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: JSON can be partially unmarshalled into a map in Go using the json.Unmarshal() function.
---

**Contents**

[TOC]

## Section 1: JSON Unmarshal
JSON Unmarshal is a process in which a JSON-formatted string is converted into a Go data structure. The data structure is usually a map, but can also be a struct, array, or any other type.

## Section 2: Go Map
A Go map is a data structure that stores key-value pairs. It is similar to a hash table or a dictionary in other languages. The keys are typically strings, and the values can be any type, including other maps.

## Section 3: Unmarshal into a Map
When unmarshaling a JSON string into a Go map, the keys of the map are determined by the names of the keys in the JSON string. The values of the map are determined by the values of the corresponding keys in the JSON string.

## Section 4: Example
For example, if the JSON string is `{"name": "John", "age": 30}`, then the Go map created by unmarshaling the JSON string would be `map[string]interface{}{"name": "John", "age": 30}`.
