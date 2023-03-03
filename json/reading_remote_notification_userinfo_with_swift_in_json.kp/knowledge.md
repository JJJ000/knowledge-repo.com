---
title: Retrieve userinfo from a remote notification using swift
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-03 00:00:00
updated_at: 2023-03-03 00:00:00
tldr: Yes, you can read the userInfo of a remote notification in JSON format.
---

**Contents**

[TOC]

1. Parsing the UserInfo

The `userInfo` dictionary of a remote notification can be parsed by using the `JSONSerialization` class. This class provides methods to convert a JSON object into a Foundation object and vice versa.

2. Deserializing the JSON

The `JSONSerialization` class can be used to deserialize the `userInfo` dictionary into a Foundation object. This can be done by using the `JSONObjectWithData:options:error:` method.

3. Accessing the UserInfo

Once the `userInfo` dictionary has been deserialized, it can be accessed by using the `objectForKey:` method. This method allows the user to access the values of the `userInfo` dictionary.

4. Error Handling

It is important to handle any errors that may occur during the deserialization process. The `JSONObjectWithData:options:error:` method returns an `NSError` object if an error occurs. This can be used to display an appropriate error message to the user.
