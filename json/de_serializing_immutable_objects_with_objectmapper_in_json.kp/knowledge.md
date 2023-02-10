---
title: What is the process for converting an immutable object without a default constructor into a serialized format using objectmapper?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use @JsonCreator and @JsonProperty annotations to manually construct an immutable object without a default constructor using ObjectMapper.
---

**Contents**

[TOC]

#### Step 1: Create a Custom Deserializer

Create a custom deserializer class that extends StdDeserializer of Jackson library. The deserializer class should override the deserialize() method, which should take in two parameters, a JsonParser object and a DeserializationContext object.

#### Step 2: Parse the Json

Using the JsonParser object, parse the Json and extract the required field values.

#### Step 3: Create an Instance of the Immutable Object

Using the extracted field values, create an instance of the immutable object using the builder pattern.

#### Step 4: Register the Deserializer

Register the custom deserializer class with an ObjectMapper object. This can be done by calling the registerModule() method of the ObjectMapper object, passing in a SimpleModule object, which in turn takes in the custom deserializer class.
