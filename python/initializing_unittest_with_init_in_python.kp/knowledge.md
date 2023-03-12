---
title: The initialization method for the unittest.testcase class
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: \_\_init\_\_ is a special method in Python classes that is called when an instance of the class is created, but it is not required in unittest.TestCase classes as they are instantiated by the testing framework.
---

**Contents**

[TOC]

1. Introduction to unittest.TestCase
unittest is a built-in Python module for testing purposes. In unittest, TestCase is a class used to create test cases for unit tests. It provides several methods and functions to test a codebase's correctness and performance.

2. __init__ method in unittest.TestCase
In Python, __init__ is a special method that gets called automatically when an object is created. Likewise, when creating test cases, *__init__* can be overridden to define the test suite's context. It is called before each test method. 

For example,

import unittest

class TestStringMethods(unittest.TestCase):
 
    def __init__(self, methodName: str) -> None:
        super().__init__(methodName=methodName)
        self.someVar = 'This is a variable'
        
    def test_upper(self):
        self.assertEqual('foo'.upper(), 'FOO')
 
    def test_isupper(self):
        self.assertTrue('FOO'.isupper())
 
    def test_split(self):
        s = 'hello world'
        self.assertEqual(s.split(), ['hello', 'world'])
 
        #Check that s.split fails when the separator is not a string
        with self.assertRaises(TypeError):
            s.split(2)
            
When creating a Test Class that will inherit from TestCase in the example above, it takes the method name which is used to name it's parent class. The  subclass TestStringMethods overrides the *__init__* method to instantiate an instance variable that is accessible to all methods within the test class. In this context, the constructor instantiates the variable `someVar` to a string object, which can be accessed by calling `self.someVar` in any other methods.

3. Overriding __init__ to instantiate class variables
The *__init__* can also be used to instantiate class variables shared among test classes. 

For example,

import unittest
 
class TestStringMethods(unittest.TestCase):
 
    name = 'Unit Test suite'
 
    def __init__(self, methodName: str) -> None:
        super().__init__(methodName=methodName)
        self.someVar = 'This is a variable'
 
    def test_upper(self):
        self.assertEqual('foo'.upper(), 'FOO')
 
    def test_isupper(self):
        self.assertTrue('FOO'.isupper())
 
    def test_split(self):
        s = 'hello world'
        self.assertEqual(s.split(), ['hello', 'world'])
 
        #Check that s.split fails when the separator is not a string
        with self.assertRaises(TypeError):
            s.split(2)
 
class TestStringMethods2(unittest.TestCase):
 
    def test_split(self):
        s = 'hello world'
        self.assertEqual(s.split(), ['hello', 'world'])
        
In the example above, the *__init__* method is used to instantiate an instance variable named `someVar`, and a class variable, `name`. This allows us to access the class variable using `TestStringMethods.name` in the code.

4. Conclusion
In unittest.TestCase, *__init__* is a special method that is a way of setting up the test suite's context, and it can be overridden to instantiate test suite's instance or class variables. This way, the variables are accessible throughout the testing suite, and it improves code readability and maintainability.
