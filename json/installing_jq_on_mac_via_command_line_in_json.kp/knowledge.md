---
title: What are the steps to install jq on mac using the command line?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Install JQ on Mac using the command line by running `brew install jq`.
---

**Contents**

[TOC]

## Downloading JQ
1. Download JQ from the official website: [https://stedolan.github.io/jq/download/](https://stedolan.github.io/jq/download/)
2. Select the appropriate version for your operating system (in this case, macOS).

## Installing JQ
1. Unzip the downloaded file.
2. Move the `jq` binary to the desired location. It is recommended to move it to a directory that is part of your system’s PATH.
3. Make sure the `jq` binary is executable by running the command `chmod +x jq`

## Testing the Installation
1. Open a new terminal window and type `jq --version` to verify that the installation was successful.
2. Try running a simple command to test the installation, such as `echo '{"foo": "bar"}' | jq '.foo'` which should output `"bar"`.
