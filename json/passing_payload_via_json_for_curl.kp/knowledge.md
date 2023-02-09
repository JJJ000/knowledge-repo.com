---
title: What is the syntax for passing a payload via a JSON file with curl?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The payload can be passed via a JSON file for curl by using the `-d @filename.json` flag.
---

**Contents**

[TOC]

1. Set Up Your JSON File

Before you can pass a payload via JSON file for curl, you will need to create your JSON file. This file should contain all the necessary data for your curl request.

2. Pass the JSON File in Your Curl Request

Once you have your JSON file set up, you can pass it in your curl request by using the `--data-binary` flag. This flag allows you to pass a file as the body of your request.

3. Set the Content-Type Header

In order for curl to properly interpret the data in your JSON file, you will need to set the `Content-Type` header to `application/json`. This can be done by using the `-H` flag.

4. Execute Your Request

Once you have your JSON file set up and your headers set, you can execute your curl request by using the `curl` command. This will send your request with the data from your JSON file as the payload.
