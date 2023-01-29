---
title: What is the process for updating all Python packages using pip?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the command `pip freeze | xargs pip install -U` to upgrade all Python packages with pip.
---

**Contents**

[TOC]

# Step 1: Updating pip

Before attempting to upgrade any packages, it is important to make sure that pip is up to date. To do this, run the following command:

`pip install --upgrade pip`

# Step 2: Listing Packages

To get a list of all packages installed with pip, run the following command:

`pip list`

# Step 3: Upgrading Packages

To upgrade all packages, run the following command:

`pip freeze --local | grep -v '^\-e' | cut -d = -f 1  | xargs -n1 pip install -U`

# Step 4: Verifying Upgrade

To verify that the upgrade was successful, run the following command:

`pip list --outdated`
