---
title: System.text.json decode unicode string in .net core
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: The System.Text.Json class does not have a built-in method to unescape unicode strings.
---

**Contents**

[TOC]

# Approach 1: Using String.Replace()

The `String.Replace()` method can be used to replace each unicode escape sequence with its corresponding unicode character. 

Example:

```csharp
string jsonString = @"{""Name"":""\u0041\u0042\u0043""}";

string unescapedString = jsonString.Replace(@"\u", "%u");
```

# Approach 2: Using Regex.Unescape()

The `Regex.Unescape()` method can be used to unescape all unicode escape sequences in a string. 

Example:

```csharp
string jsonString = @"{""Name"":""\u0041\u0042\u0043""}";

string unescapedString = Regex.Unescape(jsonString);
```

# Approach 3: Using System.Text.Json

The `System.Text.Json` library provides a `JsonSerializer.Deserialize<T>()` method which can be used to deserialize a JSON string into a strongly-typed object. This will automatically unescape all unicode escape sequences. 

Example:

```csharp
string jsonString = @"{""Name"":""\u0041\u0042\u0043""}";

MyObject obj = JsonSerializer.Deserialize<MyObject>(jsonString);
```

# Approach 4: Using Newtonsoft.Json

The `Newtonsoft.Json` library provides a `JsonConvert.DeserializeObject<T>()` method which can be used to deserialize a JSON string into a strongly-typed object. This will automatically unescape all unicode escape sequences. 

Example:

```csharp
string jsonString = @"{""Name"":""\u0041\u0042\u0043""}";

MyObject obj = JsonConvert.DeserializeObject<MyObject>(jsonString);
```
