---
title: How can I confirm that a unit test result in python/django contains a specific string?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Assert that the response.data contains the expected string using the assertIn() method.
---

**Contents**

[TOC]

# Section 1: Overview

When writing unit tests for a Django application, it is often necessary to assert that the result of the unit test contains a certain string in JSON format. This can be accomplished by using a combination of the Python `json` module and the Django `TestCase` class.

# Section 2: Importing the Necessary Modules

In order to assert that the result of a unit test contains a certain string in JSON format, the `json` module and the `TestCase` class must be imported. This can be done by adding the following lines of code to the top of the unit test script:

```python
import json
from django.test import TestCase
```

# Section 3: Asserting the JSON String

Once the necessary modules have been imported, the `assertIn` method of the `TestCase` class can be used to assert that the result of the unit test contains a certain string in JSON format. This can be done by adding the following line of code to the unit test script:

```python
self.assertIn('expected_string', json.loads(response.content))
```

# Section 4: Conclusion

By combining the Python `json` module and the Django `TestCase` class, it is possible to assert that the result of a unit test contains a certain string in JSON format. This can be accomplished by importing the necessary modules and using the `assertIn` method of the `TestCase` class.
