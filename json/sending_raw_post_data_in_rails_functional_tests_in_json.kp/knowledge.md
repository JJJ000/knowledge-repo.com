---
title: What is the process for sending raw post data in a rails functional test?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Use the body option in the post call to send raw post data in JSON format.
---

**Contents**

[TOC]

# Section 1: Setting Up the Post Request

In a Rails functional test, you can use the `post` method to send raw data in JSON. To do this, you must pass in a hash with the `:body` key set to the JSON string.

For example:

```ruby
post '/api/v1/users', 
  body: {
    user: {
      name: 'John Doe',
      email: 'jdoe@example.com'
    }
  }.to_json
```

# Section 2: Setting the Content Type Header

In order for Rails to correctly parse the JSON data, you must also set the `Content-Type` header to `application/json`. This can be done by passing a second argument to the `post` method.

For example:

```ruby
post '/api/v1/users', 
  body: {
    user: {
      name: 'John Doe',
      email: 'jdoe@example.com'
    }
  }.to_json,
  headers: { 'Content-Type': 'application/json' }
```

# Section 3: Asserting the Response

Once the request has been sent, you can use the `assert_response` method to check the response code.

For example:

```ruby
post '/api/v1/users', 
  body: {
    user: {
      name: 'John Doe',
      email: 'jdoe@example.com'
    }
  }.to_json,
  headers: { 'Content-Type': 'application/json' }

assert_response :created
```

# Section 4: Testing the Response Body

You can use the `json_response` method to test the response body. This method will parse the response body into a hash.

For example:

```ruby
post '/api/v1/users', 
  body: {
    user: {
      name: 'John Doe',
      email: 'jdoe@example.com'
    }
  }.to_json,
  headers: { 'Content-Type': 'application/json' }

assert_response :created

assert_equal 'John Doe', json_response[:user][:name]
assert_equal 'jdoe@example.com', json_response[:user][:email]
```
