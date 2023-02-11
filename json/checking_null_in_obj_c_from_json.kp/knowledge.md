---
title: Verifying if a nil value has been returned from a JSON string in objective-c
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can check if the value is null by using the `isEqualToString` method to compare the value with the string `null`.
---

**Contents**

[TOC]

## Using the NSNull Class

The NSNull class is the Objective-C equivalent of the null keyword in other languages. It can be used to check if a value returned from a JSON string is null. To check if a value is null, you can use the isEqualToString: method of NSNull and compare it to the string "null":

```objc
if ([value isEqualToString:@"null"]) {
    // Value is null
}
```

## Using the nil Constant

The nil constant is the Objective-C equivalent of the null keyword in other languages. It can be used to check if a value returned from a JSON string is null. To check if a value is null, you can use the isEqual: method of nil and compare it to the NSNull class:

```objc
if ([value isEqual: [NSNull null]]) {
    // Value is null
}
```

## Using the == Operator

The == operator can also be used to check if a value returned from a JSON string is null. To check if a value is null, you can use the == operator and compare it to the nil constant:

```objc
if (value == nil) {
    // Value is null
}
```

## Using the isKindOfClass: Method

The isKindOfClass: method of NSObject can also be used to check if a value returned from a JSON string is null. To check if a value is null, you can use the isKindOfClass: method and compare it to the NSNull class:

```objc
if ([value isKindOfClass:[NSNull class]]) {
    // Value is null
}
```
