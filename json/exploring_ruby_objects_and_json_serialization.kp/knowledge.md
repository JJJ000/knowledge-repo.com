---
title: Serializing ruby objects into JSON (without the use of rails)
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Ruby objects can be serialized to JSON using the `json` gem.
---

**Contents**

[TOC]

# Introduction

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is designed to be easy for humans to read and write. It is commonly used to serialize and transfer data between clients and servers. In Ruby, JSON can be used to serialize objects into a JSON string, and to parse a JSON string into a Ruby object.

# Serializing Ruby Objects into JSON

Ruby objects can be serialized into JSON strings using the `to_json` method. This method takes an optional argument that can be used to customize the serialization of the object. For example, the following code will serialize a Ruby hash into a JSON string:

```ruby
require 'json'

my_hash = { :name => "John", :age => 30 }
json_string = my_hash.to_json
```

The resulting JSON string will look like this:

```json
{"name":"John","age":30}
```

# Parsing JSON Strings into Ruby Objects

JSON strings can be parsed into Ruby objects using the `JSON.parse` method. This method takes a JSON string as an argument and returns a Ruby object. For example, the following code will parse a JSON string into a Ruby hash:

```ruby
require 'json'

json_string = '{"name":"John","age":30}'
my_hash = JSON.parse(json_string)
```

The resulting Ruby hash will look like this:

```ruby
{ :name => "John", :age => 30 }
```

# Conclusion

JSON is a popular data-interchange format that can be used to serialize and parse Ruby objects. The `to_json` method can be used to serialize a Ruby object into a JSON string, and the `JSON.parse` method can be used to parse a JSON string into a Ruby object.
