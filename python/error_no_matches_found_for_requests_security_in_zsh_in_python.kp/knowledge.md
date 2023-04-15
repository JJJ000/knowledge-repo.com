---
title: There are no matches found for 'requests[security]' in zsh
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The square brackets in `requests[security]` are globbing characters in zsh shell, and need to be escaped or quoted with single quotes to avoid the error.
---

**Contents**

[TOC]

Section 1: Introduction

The `zsh: no matches found` error usually occurs when you are trying to run a command using a wildcard character, and the shell is unable to find a match for it. This error can also occur when you are trying to install Python modules using pip and encounter the `requests[security]` module.

Section 2: Understanding the `zsh: no matches found: requests[security]` error

When you encounter the `zsh: no matches found: requests[security]` error in Python, it means that `pip` is unable to find the `requests[security]` module in its available repositories. This error usually occurs when you are trying to install a module that has additional requirements, such as the `requests[security]` module. In such cases, you need to install the required additional modules separately.

Section 3: Fixing the `zsh: no matches found: requests[security]` error

To fix the `zsh: no matches found: requests[security]` error, first, make sure that you have the latest version of pip installed on your system. Also, ensure that you have the required additional modules installed on your system. You can install these modules separately using the following command:

```python
pip install requests[security]
```

If you still encounter the same error, you can try using the following command:

```python
pip install requests requests[security]
```

This command installs the `requests` module and its additional requirements separately.

Section 4: Conclusion

The `zsh: no matches found: requests[security]` error in Python occurs when there is a problem installing the `requests[security]` module using pip. To fix this error, you need to ensure that you have the latest version of pip installed on your system and that the required additional modules are also installed separately. If you have followed the above steps and are still encountering the error, you may need to seek further assistance.
