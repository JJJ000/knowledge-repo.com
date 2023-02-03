---
title: What is the process for transforming an existing callback API into promises?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the library `Q` to convert existing callbacks to promises.
---

**Contents**

[TOC]

1. Identify the Callback API
The first step is to identify the existing callback API. This can be done by looking at the code and determining which functions are being used as callbacks.

2. Wrap the Callback API with a Promise
Once the callback API has been identified, the next step is to wrap it with a Promise. This can be done by creating a new function that returns a Promise and passing the callback API as an argument. The Promise should resolve or reject based on the result of the callback API.

3. Use the Promise in the Code
Once the Promise has been created, it can be used in the code in place of the callback API. This can be done by using the `.then()` and `.catch()` methods on the Promise to handle the success and failure cases respectively.

4. Test the Conversion
Finally, it is important to test the conversion to ensure that the Promise is behaving as expected. This can be done by running the code with different inputs and verifying that the correct result is being returned.
