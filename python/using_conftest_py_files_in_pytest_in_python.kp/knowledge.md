---
title: What is the purpose of conftest.py files in pytest?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Conftest.py files are used to share fixtures, variables, and other code across multiple test files in pytest.
---

**Contents**

[TOC]

# Overview
The conftest.py file is a special file used by pytest to store configuration information. It is used to store fixtures, plugins, and other customizations. It is also used to share fixtures among multiple test files. 

# Fixtures
Fixtures are functions that are used to set up and tear down a test environment. They can be used to create test data, set up test dependencies, and provide other necessary resources for tests. The conftest.py file allows fixtures to be shared among multiple test files. 

# Plugins
The conftest.py file can also be used to store plugins. Plugins are used to extend pytest’s functionality. The conftest.py file allows plugins to be shared among multiple test files. 

# Customizations
The conftest.py file can also be used to store customizations. These customizations can be used to modify the behavior of pytest. For example, customizations can be used to modify the way pytest handles assertions or to add additional logging.
