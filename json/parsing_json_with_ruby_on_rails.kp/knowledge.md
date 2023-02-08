---
title: What is the process for extracting data from a JSON file using ruby on rails?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can parse JSON with Ruby on Rails using the built-in JSON library.
---

**Contents**

[TOC]

# Section 1 - Install gem

In order to parse JSON with Ruby on Rails, you will need to install the [json](https://rubygems.org/gems/json) gem. To do this, add the following line to your `Gemfile`:

```ruby
gem 'json'
```

Then run `bundle install` to install the gem.

# Section 2 - Parse JSON with `JSON.parse`

Once the gem is installed, you can use the `JSON.parse` method to parse the JSON. This method takes a string of JSON as an argument and returns a hash containing the parsed data. For example:

```ruby
require 'json'

json_string = '{"name": "John Doe", "age": 30}'

data = JSON.parse(json_string)

puts data # => {"name"=>"John Doe", "age"=>30}
```

# Section 3 - Access data from hash

Once the JSON is parsed into a hash, you can access the data using the keys. For example:

```ruby
name = data["name"] # => "John Doe"
age = data["age"] # => 30
```

# Section 4 - Parse JSON with `ActiveSupport::JSON.decode`

If you are using Rails, you can also use the `ActiveSupport::JSON.decode` method to parse the JSON. This method takes a string of JSON and returns a hash containing the parsed data. For example:

```ruby
require 'active_support/json'

json_string = '{"name": "John Doe", "age": 30}'

data = ActiveSupport::JSON.decode(json_string)

puts data # => {"name"=>"John Doe", "age"=>30}
```
