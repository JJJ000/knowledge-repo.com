---
title: Error with ambiguous reference to 'datatask(withcompletionhandler)' when using swift 3 urlsession.shared()
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: This is a known bug in Swift 3, and is fixed in Swift 4.
---

**Contents**

[TOC]

# Section 1: Overview of the Issue
Swift 3 URLSession.shared() has an ambiguous reference to member 'dataTask(with:completionHandler:) error when working with JSON. This error occurs when developers attempt to use the dataTask(with:completionHandler:) method to retrieve data from a remote source, such as an API. The issue is that the compiler is unable to identify which version of the method should be used, leading to an ambiguous reference error.

# Section 2: Causes of the Error
The error is caused by the fact that there are two different versions of the dataTask(with:completionHandler:) method available in Swift 3. The first version takes a URLRequest object as a parameter, while the second version takes a URL and a completionHandler as parameters. Since both methods have the same name, the compiler is unable to determine which one should be used, resulting in an ambiguous reference error.

# Section 3: Solutions
The easiest way to solve this issue is to explicitly specify which version of the dataTask(with:completionHandler:) method should be used. For example, if you want to use the version that takes a URLRequest object as a parameter, you would specify the full method name: URLSession.shared().dataTask(with: URLRequest, completionHandler: completionHandler). This will ensure that the compiler knows which version of the method to use, and the error will be resolved.

# Section 4: Conclusion
The ambiguous reference to member 'dataTask(with:completionHandler:) error in Swift 3 URLSession.shared() is a common issue when working with JSON. However, it is relatively easy to solve by explicitly specifying which version of the method should be used. Doing so will ensure that the compiler knows which version of the method to use, and the error will be resolved.
