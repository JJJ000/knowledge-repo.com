---
title: Send a JSON payload to an API using the rails framework and the httparty gem
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Rails can use HTTParty to send a JSON request to an API by using the HTTParty.post() method.
---

**Contents**

[TOC]

# Section 1: Setup

Before you can post JSON to an API using Rails and HTTParty, you will need to install the HTTParty gem. To do this, add the following line to your Gemfile:

`gem 'httparty'`

Then run `bundle install` to install the gem.

# Section 2: Configure

Once the gem is installed, you will need to configure it for your Rails application. To do this, add the following line of code to your application.rb file:

`require 'httparty'`

# Section 3: Post JSON

Once the gem is installed and configured, you can use HTTParty to post JSON to the API. To do this, you can use the following code snippet:

`HTTParty.post('http://example.com/api/endpoint', :body => { :key1 => 'value1', :key2 => 'value2' }.to_json, :headers => { 'Content-Type' => 'application/json' })`

# Section 4: Response

After you have posted the JSON, you will receive a response from the API. This response will contain the status code and any data that the API returns. You can access this data by using the `parsed_response` method on the response object. For example:

`response = HTTParty.post('http://example.com/api/endpoint', :body => { :key1 => 'value1', :key2 => 'value2' }.to_json, :headers => { 'Content-Type' => 'application/json' })

data = response.parsed_response`
