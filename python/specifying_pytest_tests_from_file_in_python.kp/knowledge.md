---
title: How can I specify which pytest tests to run from a file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, you can use the `-k` flag in pytest to specify which tests to run from a file.
---

**Contents**

[TOC]

1. Using the `pytest` Command Line Options

Pytest provides a number of command line options that allow you to specify which tests to run from a file. The most common way to do this is to use the `-k` option, which allows you to specify a test name or a test expression that will be used to select tests to run. For example, if you have a file called `test_example.py` that contains tests, you can run all the tests in that file by running the following command:

```
pytest -k test_example.py
```

You can also use the `-k` option to select specific tests to run by specifying a test name or expression. For example, if you want to run all tests that contain the word “foo” in the name, you can use the following command:

```
pytest -k "foo"
```

2. Using the `pytest_collect_file` Hook

Pytest also provides a hook called `pytest_collect_file` that allows you to specify which tests to run from a file. This hook takes two arguments: a path to a test file and a list of test names. The hook will then collect all the tests in the file that match the names in the list.

For example, if you have a file called `test_example.py` and you want to run all tests that contain the word “foo” in the name, you can use the following code:

```
def pytest_collect_file(path, names):
    if path.basename == "test_example.py":
        return pytest.Module(path, names=["foo"])
```

3. Using the `pytest_runtest_setup` Hook

The `pytest_runtest_setup` hook allows you to specify which tests to run from a file. This hook takes two arguments: a test item and a list of test names. The hook will then collect all the tests in the file that match the names in the list.

For example, if you have a file called `test_example.py` and you want to run all tests that contain the word “foo” in the name, you can use the following code:

```
def pytest_runtest_setup(item, names):
    if item.fspath.basename == "test_example.py":
        item.keywords["foo"] = True
```

4. Using the `pytest_configure` Hook

The `pytest_configure` hook allows you to specify which tests to run from a file. This hook takes two arguments: a `config` object and a list of test names. The hook will then collect all the tests in the file that match the names in the list.

For example, if you have a file called `test_example.py` and you want to run all tests that contain the word “foo” in the name, you can use the following code:

```
def pytest_configure(config, names):
    config.addinivalue_line("python_files", "test_example.py:foo")
```
