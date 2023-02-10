---
title: Appending an item to a JSON object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can add a new array element to a JSON object by using the `push` method.
---

**Contents**

[TOC]

1. Access the JSON Object 

In order to add a new element to a JSON object, the object must first be accessed. Depending on the context, this can be done using various methods. For example, if the JSON object is stored in a variable, it can be accessed directly by referencing the variable.

2. Add the Element

Once the JSON object is accessed, the new element can be added. This is done by specifying the key for the element, followed by the value. For example, if the new element is an array, the syntax would look like this:

`"key": ["value1", "value2"]`

3. Stringify the Object

Once the element has been added, the object must be stringified in order to be stored or sent. This can be done using the `JSON.stringify()` method.

4. Store or Send the Object

Finally, the stringified object can be stored or sent as needed. For example, if the object is to be sent to a server, it can be done using an AJAX request.
