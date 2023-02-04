---
title: What is the distinction between 'it' and 'test' when using jest?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Jest is a JavaScript testing framework, while `it` is a Jest test function used to define and run a single test.
---

**Contents**

[TOC]

# Difference in Usage

The word 'it' is used when writing a Jest unit test to refer to the subject of the test. It is used as a placeholder for the actual code that is being tested.

The word 'test' is used to refer to a specific unit test. A test is a function that contains the code to be tested and the assertions that are used to check the results of the code.

# Difference in Syntax

The word 'it' is used to declare a test within the Jest framework. It is followed by a string that describes the test and a callback function that contains the code to be tested.

The word 'test' is used to declare a test suite within the Jest framework. It is followed by a string that describes the suite and a callback function that contains the tests to be run.

# Difference in Scope

The word 'it' is used to declare a single unit test. It is used to test a single piece of code, and the assertions are used to check the results of that code.

The word 'test' is used to declare a suite of unit tests. It is used to test multiple pieces of code, and the assertions are used to check the results of each piece of code.
