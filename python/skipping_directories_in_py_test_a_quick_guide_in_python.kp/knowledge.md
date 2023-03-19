---
title: What is the procedure for instructing py.test to exclude specific directories?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Mark the directories with a `pytest.ini` file containing the line `addopts=-rs --ignore=path/to/directory`.
---

**Contents**

[TOC]

## Section 1: Using command line option

One way to tell py.test to skip certain directories is to use a command line option. The option `--ignore` can be used to specify a directory or a pattern of directories to be ignored by py.test.

For example, to skip the directory `tests/skip`, we can run py.test with the command:

```
python -m pytest --ignore=tests/skip
```

## Section 2: Using pytest.ini

Another way to skip certain directories is to use a pytest.ini file. We can create a pytest.ini file in the root directory of our project and specify the directories to be skipped using the `addopts` option.

To skip the directory `tests/skip`, we can add the following line to the pytest.ini file:

```
[pytest]
addopts = --ignore=tests/skip
```

## Section 3: Using marks

Marks can also be used to skip certain directories in py.test. We can create a custom marker in the conftest.py file and use it to mark the test functions in the directory we want to skip.

For example, we can add the following code to the conftest.py file:

```
import pytest

@pytest.mark.skip(reason="Tests in this directory are incomplete.")
def test_directory():
    pass
```

This will skip all the tests in the directory that contains the test_directory() function.

## Section 4: Using fixture

Finally, we can use a fixture to skip certain directories in py.test. We can create a fixture in the conftest.py file that checks whether the test file belongs to a specific directory and skip the test if it does.

For example, we can add the following code to the conftest.py file:

```
import pytest

@pytest.fixture()
def skip_directory(request):
    if "tests/skip" in str(request.fspath):
        pytest.skip("Tests in this directory are skipped.")
```

This fixture can then be used in the test files to skip the tests in the specified directory:

```
def test_example(skip_directory):
    assert True
```

This will skip the test if it belongs to the `tests/skip` directory.
