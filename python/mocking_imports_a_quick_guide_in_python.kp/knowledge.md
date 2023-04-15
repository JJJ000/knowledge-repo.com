---
title: What is the process to create a mock import?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the unittest.mock module to patch the import statement with a mock object.
---

**Contents**

[TOC]

## Introduction
Unit tests are an essential part of software development. However, sometimes the code being tested depends on external libraries or modules. In these cases, if you want to isolate the unit test from the external dependencies, you can use mocking. In this article, we will learn how to mock an import in Python.

## Using the unittest.mock library
The `unittest.mock` library provides a powerful yet simple way to mock objects and functions. Specifically, `unittest.mock.patch` is the main class used to mock an import in Python. The patch function is a context manager that temporarily replaces an object with a mock object.

```python
import unittest.mock as mock

with mock.patch('module.myfunction') as mock_myfunction:
    mock_myfunction.return_value = 42
    #code that uses myfunction
```
The `patch` method can take any import as its argument, and it mocks alternative temporary attributes and methods with the `spec` argument.


## Using the magic method
Alternatively, we can overwrite the `__import__` function with a mock function that returns a mock object:

```python
import types
import sys

class MockModule(types.ModuleType):
    def __getattr__(self, name):
        return None

def noop_import(*args):
    if len(args) > 3:
        return MockModule(args[0])
    return __import__(*args)

sys.modules[__name__].__setattr__('__import__', noop_import) # Mock the import
```
In this approach, we define a mock class that always returns None when an attribute is access. Then, we replace the `__import__` method in the `sys` module with our custom function that always returns a mock module.

## Using the Pytest Monkeypatch Fixture
Pytest offers a `monkeypatch` fixture that allows patching Python attributes, dictionary keys, environment variables, and functions. Import Patching is done by calling method `monkeypatch.setattr()` method to substitute attributes.
```python
def test_database(monkeypatch):
    class MockDatabase:
        def connect(self):
            return 'mocked database'
    
    def mockreturn(*args, **kwargs):
        return MockDatabase()

    monkeypatch.setattr(Database, 'connect', mockreturn)
    
    # test code that uses the Database class
```
In this code, we have mocked the `Database` class object's connect method. Pytest monkeypatch fixture does this on a per-test function basis, making it ideal for testing custom replacement behaviors.

## Conclusion
Mocking an import in Python is very important when a module or package's availability, speed, quality or reliability is in doubt or when testing. We covered three ways to mock an import in Python: using the `unittest.mock` library, using the magic method approach, and using the Pytest monkeypatch fixture. Choose the technique that best suits the testing needs of your project.
