---
title: What is the reason for boost property tree's write_json function to store all values as strings? is it possible to modify this behavior?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: No, it is not possible to change that, as Boost Property Tree is designed to save all data as strings.
---

**Contents**

[TOC]

## Overview
Boost property tree is a library used to store and parse hierarchical data. It is used to parse JSON, XML, and INI files. The library provides a `write_json` function which is used to write data to a JSON file. However, the function saves all data as strings, regardless of the data type. It is possible to change this behavior.

## Reasons for Saving as Strings
The main reason why Boost property tree saves all data as strings is to maintain compatibility with the JSON format. The JSON format only allows strings, numbers, booleans, objects, and arrays. Other data types, such as dates and times, are not supported. Therefore, Boost property tree must convert all other data types to strings in order to maintain compatibility with the JSON format.

## Changing the Behavior
It is possible to change the behavior of the `write_json` function so that it saves data in its original data type. This can be done by using the `boost::property_tree::json_parser::write_json` function instead of the `boost::property_tree::write_json` function. The `json_parser::write_json` function can save data in its original data type.

## Conclusion
Boost property tree saves all data as strings in order to maintain compatibility with the JSON format. However, it is possible to change this behavior by using the `boost::property_tree::json_parser::write_json` function instead of the `boost::property_tree::write_json` function.
