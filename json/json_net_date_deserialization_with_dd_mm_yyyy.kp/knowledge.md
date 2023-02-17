---
title: Using json.net to deserialize dates in the dd/mm/yyyy format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Json.Net can deserialize dates with dd/MM/yyyy format using the DateFormatString property.
---

**Contents**

[TOC]

#### Section 1: Adding a Custom JsonConverter

The first step in deserializing dates with dd/MM/yyyy format using Json.Net is to create a custom JsonConverter. This JsonConverter will be used to override the default behavior of Json.Net when it encounters a date string.

#### Section 2: Implementing the ReadJson Method

Once the custom JsonConverter is created, the next step is to implement the ReadJson method. This method will take in a JsonReader and deserialize the date string into a DateTime object. The date string can then be parsed using the DateTime.ParseExact method, which takes in the date string and the format string.

#### Section 3: Setting the JsonSerializerSettings

The final step is to set the JsonSerializerSettings to use the custom JsonConverter. This can be done by creating a new instance of JsonSerializerSettings and setting the Converters property to a list containing the custom JsonConverter.

#### Section 4: Deserializing the Date

Once the JsonSerializerSettings is set, the date can now be deserialized using the JsonConvert.DeserializeObject method. This method takes in the date string and the JsonSerializerSettings and returns a DateTime object.
