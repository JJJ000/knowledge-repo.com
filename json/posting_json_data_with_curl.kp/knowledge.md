---
title: What is the command to use curl to send json data?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-13 00:00:00
updated_at: 2023-01-13 00:00:00
tldr: Use the `-H` flag to specify the content type as `application/json` and the `-d` flag to provide the JSON data as a string.
---

**Contents**

[TOC]

### Create a File with JSON Data

Create a file with the JSON data that you would like to POST. For example, if you would like to POST the following JSON data:

```json
{
  "name": "John Doe",
  "age": 30
}
```

Create a file named `data.json` with the following content:

```json
{
  "name": "John Doe",
  "age": 30
}
```

### Set the Content-Type Header

Set the `Content-Type` header to `application/json` in your cURL request. For example:

```shell
curl -H "Content-Type: application/json"
```

### Use the --data Option

Use the `--data` option to POST the JSON data. For example:

```shell
curl --data @data.json
```

### Execute the Request

Execute the cURL request. For example:

```shell
curl -H "Content-Type: application/json" --data @data.json http://example.com/api
```
