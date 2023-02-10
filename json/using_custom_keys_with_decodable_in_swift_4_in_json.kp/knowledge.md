---
title: What is the process for incorporating custom keys when using swift 4's decodable protocol?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the CodingKeys enum to map the custom keys to the properties of the Decodable type.
---

**Contents**

[TOC]

## Section 1: Create Model

To use custom keys with Swift 4's Decodable protocol in JSON, you must first create a model that conforms to the Decodable protocol. This model should include all of the data that you want to decode from the JSON. 

## Section 2: Specify Keys

Next, you must specify the keys that you want to use to decode the data. This is done by adding a CodingKeys enumeration to your model. The CodingKeys enumeration should include a case for each of the keys that you want to use for decoding. 

## Section 3: Map Keys

Once you have specified the keys, you must map them to the properties in your model. This is done by implementing the init(from decoder: Decoder) method in your model. In this method, you will use the decode(_:forKey:) method to decode the data from the JSON and assign it to the appropriate properties in your model. 

## Section 4: Decode Data

Finally, you can use the JSONDecoder class to decode the data from the JSON. The JSONDecoder class has a decode(_:from:) method that takes in a type conforming to Decodable and a Data object. This will return an instance of your model with the data decoded from the JSON.
