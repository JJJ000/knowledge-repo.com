---
title: What is the best way to convert a JSON string into an nsdictionary on ios 5 or later?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the NSJSONSerialization class to deserialize a JSON string into an NSDictionary.
---

**Contents**

[TOC]

# Section 1: Importing the Necessary Libraries

In order to deserialize a JSON string into an NSDictionary, one must first import the necessary libraries. This can be done by adding the following code to the top of your file:

```
#import <Foundation/Foundation.h>
#import <UIKit/UIKit.h>
```

# Section 2: Converting the JSON String to an NSData Object

Once the necessary libraries have been imported, the JSON string must be converted to an NSData object. This can be done by using the following code:

```
NSData *data = [jsonString dataUsingEncoding:NSUTF8StringEncoding];
```

# Section 3: Deserializing the NSData Object

Once the JSON string has been converted to an NSData object, the data can be deserialized into an NSDictionary. This can be done by using the following code:

```
NSDictionary *dictionary = [NSJSONSerialization JSONObjectWithData:data options:NSJSONReadingMutableContainers error:nil];
```

# Section 4: Accessing the Deserialized Data

Once the NSData object has been deserialized into an NSDictionary, the data can be accessed by using the following code:

```
NSString *value = [dictionary objectForKey:@"key"];
```
