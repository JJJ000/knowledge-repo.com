---
title: Store activerecord data as JSON instead of yaml
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: ActiveRecord can serialize data to JSON using the `as\_json` method.
---

**Contents**

[TOC]

## Section 1: Enabling JSON Serialization

ActiveRecord provides a way to serialize objects to JSON by setting the `ActiveRecord::Base.include_root_in_json` configuration option to `true`. This allows ActiveRecord to include the model name in the JSON output.

## Section 2: Creating the Serializer

Once the configuration option is set, a serializer needs to be created. This can be done by creating a class that inherits from `ActiveModel::Serializer`. The class should define the attributes and associations to be serialized.

## Section 3: Using the Serializer

The serializer can then be used by calling the `to_json` method on the object. This will return the object serialized to JSON.

## Section 4: Example

For example, if a model named `Book` has the attributes `title` and `author`, the following serializer could be used:

```ruby
class BookSerializer < ActiveModel::Serializer
  attributes :title, :author
end
```

The serialized JSON can then be retrieved by calling `Book.first.to_json`.
