---
title: What steps should I take to turn off logging when executing Python django unit tests?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Set the logging level to a level that disables logging, such as `logging.CRITICAL` or `logging.NOTSET`.
---

**Contents**

[TOC]

## Introduction
When running unit tests in Django, it's helpful to disable logging to reduce the amount of noise in the test output. Logging can be disabled for specific tests or for the entire test suite.

## Disabling logging for specific tests
To disable logging for specific tests, you can use the `override_settings` decorator to temporarily set the `LOGGING` setting to an empty dictionary. For example:

```python
from django.test import TestCase, override_settings
import logging

class MyTestCase(TestCase):
    @override_settings(LOGGING={})
    def test_my_logging_code(self):
        # Your test code here
        pass
```

This will disable all logging for the duration of the `test_my_logging_code` method.

## Disabling logging for the entire test suite
To disable logging for the entire test suite, you can create a custom test runner that overrides the `setup_test_environment` method to disable logging. For example:

```python
from django.test.runner import DiscoverRunner

class NoLoggingTestRunner(DiscoverRunner):
    def setup_test_environment(self, **kwargs):
        super().setup_test_environment(**kwargs)
        logging.disable(logging.CRITICAL)
```

Then, in your `settings.py`, set the `TEST_RUNNER` setting to point to your custom test runner:

```python
TEST_RUNNER = 'path.to.NoLoggingTestRunner'
```

This will disable all logging for the duration of the test suite.

## Conclusion
Disabling logging while running unit tests in Django can reduce the amount of noise in the test output and make it easier to identify actual test failures. Whether you need to disable logging for specific tests or for the entire test suite, Django provides easy ways to do it.
