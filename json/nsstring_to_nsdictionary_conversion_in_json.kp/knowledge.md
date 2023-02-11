---
title: Transforming an nsstring into an nsdictionary/json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the NSJSONSerialization class to convert an NSString to an NSDictionary or JSON.
---

**Contents**

[TOC]

1. Parsing the NSString to JSON
--------------------------------
The NSString can be parsed to JSON by using the `NSJSONSerialization` class. This class provides a method, `JSONObjectWithData`, which takes an NSData object as an argument and returns an NSDictionary or NSArray depending on the data passed. To use this method, the NSString must first be converted to an NSData object. This can be done by using the `dataUsingEncoding` method on the NSString, passing in the NSUTF8StringEncoding constant.

2. Creating an NSDictionary from JSON
------------------------------------
Once the NSString has been parsed to JSON, an NSDictionary can be created from it. This can be done by using the `dictionaryWithObjectsAndKeys` method. This method takes a variable number of arguments, alternating between objects and keys. The objects must be of type id, and the keys must be of type NSString. The last argument must be nil to indicate the end of the list.

3. Accessing Values in the NSDictionary
---------------------------------------
Once the NSDictionary has been created, values can be accessed from it by using the `objectForKey` method. This method takes an NSString as an argument and returns the corresponding value if it exists in the dictionary.

4. Error Handling
-----------------
When parsing the NSString to JSON, it is important to check for errors. This can be done by using the `error` parameter of the `JSONObjectWithData` method. If an error is returned, it should be handled appropriately.
