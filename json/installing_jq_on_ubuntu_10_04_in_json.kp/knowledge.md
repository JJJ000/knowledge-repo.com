---
title: Install the jq JSON processor package on ubuntu 10.04
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Run `sudo apt-get install jq` to install jq on Ubuntu 10.04.
---

**Contents**

[TOC]

# Install jq
1. Download the jq binary from the [jq downloads page](https://stedolan.github.io/jq/download/).
2. Extract the downloaded file with the command `tar -xzf jq-<version>`.
3. Move the extracted jq binary to the /usr/local/bin directory by running `sudo mv jq-<version>/jq /usr/local/bin`.
4. Make the jq binary executable by running `sudo chmod +x /usr/local/bin/jq`.

# Verify Installation
1. Run `jq --version` to verify that jq was installed correctly.
2. You should see the version number of jq that was installed.
