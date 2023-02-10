---
title: What is the syntax for testing a JSON response using rspec?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can check for a JSON response using RSpec in Json by using the `expect(response.body).to be\_json` matcher.
---

**Contents**

[TOC]

# Section 1: Setup

1. Add the `rspec-json_matcher` gem to your Gemfile:
```
gem 'rspec-json_matcher'
```

2. Require the gem in your `spec_helper.rb` file:
```
require 'rspec/json_matcher'
```

# Section 2: Writing the Test

1. Create a test that expects a valid JSON response:
```
describe 'GET /users' do
  it 'returns a valid JSON response' do
    get '/users'
    expect(response.content_type).to eq('application/json')
    expect(response.body).to be_valid_json
  end
end
```

# Section 3: Verifying the Response

1. Add an assertion to check the response body against a predefined expected response:
```
describe 'GET /users' do
  it 'returns a valid JSON response' do
    get '/users'
    expect(response.content_type).to eq('application/json')
    expect(response.body).to be_valid_json
    expected_response = {
      'users' => [
        { 'id' => 1, 'name' => 'John Doe' },
        { 'id' => 2, 'name' => 'Jane Doe' }
      ]
    }
    expect(response.body).to match_json_expression(expected_response)
  end
end
```

# Section 4: Verifying the Response Structure

1. Add an assertion to check the response body against a predefined expected response structure:
```
describe 'GET /users' do
  it 'returns a valid JSON response' do
    get '/users'
    expect(response.content_type).to eq('application/json')
    expect(response.body).to be_valid_json
    expected_response = {
      'users' => [
        { 'id' => Integer, 'name' => String }
      ]
    }
    expect(response.body).to match_json_expression(expected_response)
  end
end
```
