---
title: Set jsonreader to lenient mode with jsonreader.setlenient(true) to allow malformed JSON to be processed at line 1, column 1, and path $
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Setting JsonReader.setLenient(true) will allow malformed JSON to be accepted.
---

**Contents**

[TOC]

# Overview

JsonReader.setLenient(true) is a method that can be used to accept malformed JSON at line 1 column 1 path $. It is available in the Android SDK and is used to tell the JsonReader to relax its strict standards for validating JSON and accept inputs that don't strictly adhere to the JSON specification.

# Advantages

Using JsonReader.setLenient(true) can be beneficial in certain scenarios, such as when dealing with user-generated content that may not be strictly compliant with the JSON specification. This can help reduce the amount of time spent validating user-generated JSON and can improve the user experience by allowing inputs that may not be strictly compliant with the specification.

# Disadvantages

Using JsonReader.setLenient(true) can also be disadvantageous in certain scenarios, such as when dealing with large amounts of data that must adhere to a strict JSON specification. In these cases, using the JsonReader.setLenient(true) can lead to data loss or corruption due to the relaxed standards for validating JSON.

# Conclusion

JsonReader.setLenient(true) can be a useful tool when dealing with user-generated content that may not be strictly compliant with the JSON specification. However, it should be used with caution when dealing with large amounts of data that must adhere to a strict JSON specification, as it can lead to data loss or corruption.
