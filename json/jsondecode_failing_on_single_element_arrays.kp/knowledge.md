---
title: Decoding an array using swift jsondecode will not work if the decoding of a single element fails
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: No, it will not fail; it will simply skip the element that failed to decode.
---

**Contents**

[TOC]

## Section 1: Overview 
When using the Swift `JSONDecoder` to decode JSON data, decoding will fail if a single element decoding fails. If a single element fails, the entire array will fail to be decoded. 

## Section 2: Reasons
The `JSONDecoder` will throw an error when a single element fails to decode. This is because the `JSONDecoder` is designed to decode a single element at a time and will not continue to decode the rest of the array if a single element fails. 

## Section 3: Solutions
One solution to this issue is to first decode the array as a `[[String: Any]]` instead of a `[Decodable]`. This will allow the `JSONDecoder` to decode the array without throwing an error. Once the array is decoded, it can then be looped through and each element can be individually decoded into its respective model. 

Another solution is to use the `JSONDecoder`'s `keyDecodingStrategy` and `nonConformingFloatDecodingStrategy` to allow the `JSONDecoder` to ignore certain types of errors and continue decoding the array. 

## Section 4: Conclusion
In conclusion, when using the Swift `JSONDecoder` to decode JSON data, decoding will fail if a single element decoding fails. There are solutions to this issue, such as decoding the array as a `[[String: Any]]` and looping through the array to individually decode each element, or using the `JSONDecoder`'s `keyDecodingStrategy` and `nonConformingFloatDecodingStrategy` to allow the `JSONDecoder` to ignore certain types of errors and continue decoding the array.
