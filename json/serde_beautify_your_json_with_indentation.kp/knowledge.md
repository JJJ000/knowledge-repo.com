---
title: Create well-formatted JSON using serde's indentation feature
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the `serde\_jsonto\_string\_pretty` method to generate pretty JSON with indentation using serde in Rust.
---

**Contents**

[TOC]

# Introduction

Serde is a Rust library that enables serialization and deserialization of Rust data structures. It provides a simple way to work with JSON data in Rust language. 

In this tutorial, we will learn how to generate pretty (indented) JSON with serde in Json.

# Importing serde and serde_json libraries

Before we begin, we need to import serde and serde_json libraries in our Rust code. Add the following lines at the beginning of your Rust code:

```rust
use serde::{Serialize, Deserialize};
use serde_json::{Result, Value};
```
 
# Generating pretty JSON

By default, serde_json library generates compact JSON formatted strings. However, we can configure serde_json to generate pretty (indented) JSON strings by using the `serde_json::to_string_pretty` function. 

Here is an example Rust program that generates pretty JSON:

```rust
use serde_json::{Result, Value};

fn main() -> Result<()> {
    let data = r#"{
        "name": "John Doe",
        "age": 32,
        "is_retired": false,
        "hobbies": ["golf", "reading", "traveling"],
        "address": {
            "street": "123 Main St",
            "city": "New York",
            "state": "NY",
            "zip": "10001"
        }
    }"#;

    let json: Value = serde_json::from_str(data)?;

    let pretty_json = serde_json::to_string_pretty(&json)?;

    println!("{}", pretty_json);

    Ok(())
}
```

In this code, we have a JSON string stored in the `data` variable. We deserialize the JSON string to a `Value` variable `json`using serde_json's `from_str` function.

Then, we use `serde_json::to_string_pretty` function to generate pretty (indented) JSON string `pretty_json` from `json`.

Finally, we print the pretty_json to the console.

# Conclusion

In this tutorial, we learned how to generate pretty (indented) JSON with serde in Json. We used serde_json’s `to_string_pretty` function to generate pretty JSON. 

By following this tutorial, you should now be able to generate beautiful and readable JSON output, which is especially useful when working with large or complex JSON data structures.
