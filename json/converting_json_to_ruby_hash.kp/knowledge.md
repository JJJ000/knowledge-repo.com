---
title: What is the process for transforming JSON into a ruby hash?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can use the JSON.parse method to convert a JSON string to a Ruby hash.
---

**Contents**

[TOC]

# Section 1: Install the JSON Gem

In order to convert JSON to a Ruby hash, you will need to install the JSON gem. This can be done by running the following command in your terminal:

```
gem install json
```

# Section 2: Load the JSON Gem

Once the JSON gem is installed, you will need to load it in your Ruby program. This can be done by adding the following line of code to your program:

```ruby
require 'json'
```

# Section 3: Parse the JSON

Next, you will need to parse the JSON string into a Ruby hash. This can be done by using the `JSON.parse` method, which takes a string argument and returns a hash.

For example, you could parse a JSON string like this:

```ruby
json_string = '{"name":"John","age":30}'
parsed_json = JSON.parse(json_string)
```

# Section 4: Access the Hash

Once the JSON string has been parsed, you can access the values of the hash by using the corresponding key. For example, if you wanted to access the name of the person in the above example, you could do the following:

```ruby
name = parsed_json["name"]
```

And the value of `name` would be `John`.
