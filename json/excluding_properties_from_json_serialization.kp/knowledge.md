---
title: What is the best way to prevent a property from being included in a JSON serialization?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the [JsonIgnore] attribute on the property to exclude it from Json Serialization.
---

**Contents**

[TOC]

1. Using the [JsonIgnore] Attribute 

The [JsonIgnore] attribute can be used to exclude a property from serialization. This attribute can be applied to a property, a field, or a method.

Example:

```
public class MyClass
{
   public string MyProperty { get; set; }
   [JsonIgnore]
   public string MyIgnoredProperty { get; set; }
}
```

2. Using the [JsonProperty] Attribute 

The [JsonProperty] attribute can be used to exclude a property from serialization by setting the `IsIgnored` property to `true`.

Example:

```
public class MyClass
{
   public string MyProperty { get; set; }
   [JsonProperty(IsIgnored = true)]
   public string MyIgnoredProperty { get; set; }
}
```

3. Using the [JsonIgnore] Attribute on Getters and Setters 

The [JsonIgnore] attribute can also be used to exclude a property from serialization by applying it to the getter and setter of the property.

Example:

```
public class MyClass
{
   private string _myIgnoredProperty;
   public string MyProperty { get; set; }

   [JsonIgnore]
   public string MyIgnoredProperty
   {
      get { return _myIgnoredProperty; }
      set { _myIgnoredProperty = value; }
   }
}
```

4. Using the [JsonIgnore] Attribute on the Class 

The [JsonIgnore] attribute can also be used to exclude a class from serialization by applying it to the class.

Example:

```
[JsonIgnore]
public class MyClass
{
   public string MyProperty { get; set; }
   public string MyIgnoredProperty { get; set; }
}
```
