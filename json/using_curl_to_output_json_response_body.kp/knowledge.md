---
title: How can I use curl to display only the JSON response body and not the http headers?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the `-s` or `--silent` flag to suppress all output except the response body.
---

**Contents**

[TOC]

### Section 1: Install cURL

cURL is a command line tool for transferring data with URL syntax. It is pre-installed in Mac OS and Linux, but you will need to install it on Windows.

### Section 2: Set cURL Options

Once cURL is installed, you can set various options to control the output of the command. To output only the HTTP response body (JSON) and no other headers etc, you can use the following command: 

```
curl -s -H "Accept: application/json" -X GET <url>
```

This command will output only the JSON response body and no other headers etc.

### Section 3: Output JSON

Once the command is executed, the response body will be printed in the terminal. This response body is in JSON format.

### Section 4: Parse JSON

If you want to parse the JSON response, you can use a JSON parser such as jq or json-c. These tools will help you to parse the JSON response and extract the data you need.
