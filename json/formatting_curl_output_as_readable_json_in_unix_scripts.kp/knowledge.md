---
title: Show curl results in a readable JSON format within a unix shell script
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: curl can be used with the -w/--write-out option to output the response in JSON format.
---

**Contents**

[TOC]

## Section 1 - Install jq

The first step is to install the `jq` command line utility. `jq` is a lightweight and flexible command line JSON processor. 

On Linux, you can install `jq` with your package manager:

```bash
$ sudo apt-get install jq
```

On Mac OS X, you can install `jq` with [Homebrew](http://brew.sh/):

```bash
$ brew install jq
```

## Section 2 - Formatting with jq

Once `jq` is installed, you can use it to format the output of `curl` commands. For example, if you have a JSON response from a `curl` command stored in a file called `response.json`, you can format it with `jq` like this:

```bash
$ jq . < response.json
```

This will output the contents of `response.json` in a nicely formatted and readable JSON format.

## Section 3 - Piping Output

You can also pipe the output of `curl` directly into `jq` for formatting. For example, if you have a `curl` command that returns a JSON response, you can pipe it directly into `jq` like this:

```bash
$ curl http://example.com/api | jq .
```

This will output the response from `curl` in a nicely formatted and readable JSON format.

## Section 4 - Output to File

You can also pipe the output of `curl` directly into `jq` and save the output to a file. For example, if you have a `curl` command that returns a JSON response, you can pipe it directly into `jq` and save the output to a file like this:

```bash
$ curl http://example.com/api | jq . > response.json
```

This will output the response from `curl` in a nicely formatted and readable JSON format, and save the output to the file `response.json`.
