---
title: Send a JSON request using ruby
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Yes, Ruby can send JSON requests using the built-in JSON library.
---

**Contents**

[TOC]

## Section 1: Creating a JSON Request

Creating a JSON request in Ruby is fairly straightforward. You can use the `JSON` library to create a JSON object.

```ruby
require 'json'

data = {
  "name" => "John Doe",
  "age" => 25
}

json_data = JSON.generate(data)
```

## Section 2: Sending the Request

Once you have created the JSON request, you can use a library such as `Net::HTTP` to send the request.

```ruby
require 'net/http'

uri = URI('http://example.com/api')

http = Net::HTTP.new(uri.host, uri.port)

request = Net::HTTP::Post.new(uri.path, 'Content-Type' => 'application/json')
request.body = json_data

response = http.request(request)
```

## Section 3: Parsing the Response

Once you have sent the request, you can use the `JSON` library to parse the response.

```ruby
require 'json'

response_data = JSON.parse(response.body)
```

## Section 4: Error Handling

It is important to handle any errors that may occur when sending the request or parsing the response.

```ruby
begin
  # Send the request
  response = http.request(request)

  # Parse the response
  response_data = JSON.parse(response.body)
rescue JSON::ParserError => e
  # Handle the parsing error
rescue StandardError => e
  # Handle any other errors
end
```
