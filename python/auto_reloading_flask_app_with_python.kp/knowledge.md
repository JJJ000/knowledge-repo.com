---
title: Automatically restarting a Python flask application after any code modifications
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Flask can be configured to automatically reload the application whenever code changes are detected.
---

**Contents**

[TOC]

# Section 1: Setup

In order to enable auto reloading of a python Flask app upon code changes, the following steps should be taken:

1. Install the Flask-Monitor extension.
2. Configure the Flask-Monitor extension in the application's configuration file.

# Section 2: Flask-Monitor

The Flask-Monitor extension is a Flask extension that provides auto reloading of a python Flask app upon code changes. It is available on the PyPI repository and can be installed with the following command:

```pip install Flask-Monitor```

# Section 3: Configuration

Once the Flask-Monitor extension is installed, it needs to be configured in the application's configuration file. The following configuration parameters need to be set:

* `MONITOR_ENABLED` – this parameter should be set to `True` to enable auto reloading.
* `MONITOR_IGNORE_PATTERNS` – this parameter should be set to a list of file patterns that should be ignored when auto reloading.
* `MONITOR_EXCLUDE_PATTERNS` – this parameter should be set to a list of file patterns that should be excluded when auto reloading.

# Section 4: Usage

Once the Flask-Monitor extension is configured, it can be used in the application by adding the following line of code to the application's main module:

```from flask_monitor import monitor```

This will enable the auto reloading of the application upon code changes.
