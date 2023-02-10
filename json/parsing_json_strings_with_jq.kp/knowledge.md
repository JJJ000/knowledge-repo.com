---
title: What are some methods for parsing a JSON string using jq (or other alternatives)?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: jq can be used to parse a JSON String by using the `jq` command followed by a filter expression.
---

**Contents**

[TOC]

# Section 1: Installing jq

jq is a command-line JSON processor that can be used to parse a JSON string. It can be installed on Mac, Linux and Windows systems. To install jq, you can use a package manager like Homebrew on Mac, apt-get on Ubuntu or Chocolatey on Windows.

# Section 2: Parsing a JSON String

Once jq is installed, you can parse a JSON string with the following command:

`jq '<JSON string>'`

For example, if the JSON string is:

`{ "name": "John", "age": 30 }`

You can parse it with the following command:

`jq '{ "name": "John", "age": 30 }'`

# Section 3: Outputting the Parsed JSON

Once the JSON string is parsed, you can output the parsed JSON in various formats. For example, you can output the parsed JSON as a compact string, a single line or an indented string.

To output the parsed JSON as a compact string, use the following command:

`jq -c '<JSON string>'`

To output the parsed JSON as a single line, use the following command:

`jq -s '<JSON string>'`

To output the parsed JSON as an indented string, use the following command:

`jq -M '<JSON string>'`

# Section 4: Alternatives to jq

If you don't want to install jq, there are other alternatives you can use to parse a JSON string. For example, you can use Python's json module, JavaScript's JSON.parse() method or Ruby's JSON.parse() method.
