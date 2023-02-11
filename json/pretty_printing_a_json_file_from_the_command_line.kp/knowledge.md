---
title: What is the best way to format a JSON file in a presentable way using the command line?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can pretty-print a JSON file from the command line in Json using the command `json\_pp filename.json`.
---

**Contents**

[TOC]

# Section 1: Install jq

The first step to pretty-printing a JSON file from the command line is to install jq. jq is a lightweight and flexible command-line JSON processor. It is available for Linux, macOS, and Windows.

# Section 2: Run the jq command

Once jq is installed, you can run the following command to pretty-print a JSON file from the command line:

`cat <filename>.json | jq .`

This will print the contents of the JSON file in an indented, human-readable format.

# Section 3: Output to a file

If you would like to output the pretty-printed JSON to a file, you can use the following command:

`cat <filename>.json | jq . > <output_filename>.json`

This will create a new file with the same name as the original file, but with the pretty-printed version of the JSON.

# Section 4: Additional Options

jq also has a number of additional options that you can use to customize the output. For example, you can use the `--sort-keys` option to sort the keys in the output. For more information about jq and its options, you can refer to the [jq manual](https://stedolan.github.io/jq/manual/).
