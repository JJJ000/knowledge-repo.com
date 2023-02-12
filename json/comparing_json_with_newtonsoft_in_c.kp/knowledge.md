---
title: Determine and return the discrepancies between two JSON objects using newtonsoft's JSON library in c#
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Newtonsoft`s Json.NET library can be used to find and return the differences between two JSON objects in C#.
---

**Contents**

[TOC]

## Section 1: Retrieving the JSON

The first step in finding the differences using Newtonsoft in C# in JSON is to retrieve the JSON. This can be done by using the JsonConvert.DeserializeObject() method. This method takes a string representing the JSON and returns an object which can be used to access the JSON's data.

## Section 2: Comparing the JSON

Once the JSON has been retrieved, it can be compared to another JSON. This can be done by using the JToken.DeepEquals() method. This method takes two JToken objects (which can be created from the DeserializeObject() method) and compares them to determine if they are equal or not. 

## Section 3: Finding the Differences

If the two JSONs are not equal, then the differences can be found by using the JToken.DeepCompare() method. This method takes two JToken objects and returns a Dictionary object that contains the differences between the two JSONs.

## Section 4: Outputting the Differences

Finally, the differences can be outputted by iterating through the Dictionary object returned by the DeepCompare() method and outputting the differences. This can be done by using a foreach loop to iterate through the Dictionary object and outputting the differences.
