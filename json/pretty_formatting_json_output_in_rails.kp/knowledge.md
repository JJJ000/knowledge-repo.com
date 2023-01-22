---
title: What is the best way to format JSON output in Ruby on Rails in an attractive manner?
authors:
- cool_wizard
tags:
- ruby
- rails
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-22 00:00:00
updated_at: 2023-01-22 00:00:00
tldr: Use the `JSON.pretty_generate` method to format JSON output in Ruby on Rails.
---

**Contents**

[TOC]

### Using the `jbuilder` Gem

The `jbuilder` gem is a great way to format JSON output in Ruby on Rails. It allows you to create a template that will generate the JSON output, and you can use it to easily add formatting and structure to the output.

### Setting the Content-Type Header

In order to ensure that the JSON output is properly formatted, you need to set the Content-Type header to `application/json`. You can do this in your controller or in your view.

### Using the `to_json` Method

In addition to using the `jbuilder` gem, you can also use the `to_json` method to format your JSON output. This method takes an object and returns a string representation of the object in JSON format.

### Using the `JSON.pretty_generate` Method

The `JSON.pretty_generate` method takes a JSON string and returns a “pretty” version of the string. This means that the output will be formatted with indentation and line breaks, making it easier to read.
