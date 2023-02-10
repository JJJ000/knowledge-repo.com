---
title: What is the process for customizing the to_json method in rails?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Override the to\_json method in a model by defining a method with the same name in the model class.
---

**Contents**

[TOC]

### Step 1: Create a Custom Serializer

The first step in overriding the `to_json` method in Rails is to create a custom serializer. This serializer should be a class that inherits from `ActiveModel::Serializer`.

### Step 2: Implement the to_json Method

Once the custom serializer is created, the `to_json` method should be implemented. This method should accept an optional options hash and return a string representation of the object.

### Step 3: Override the Default to_json Method

Once the custom `to_json` method is implemented, it should be used to override the default `to_json` method. This can be done by adding the following code to the model:

```ruby
def to_json(options = nil)
  MyCustomSerializer.new(self).to_json(options)
end
```

### Step 4: Use the Overridden to_json Method

Finally, the overridden `to_json` method can be used as needed. This can be done by calling the `to_json` method on the object or by passing the object to the `JSON.generate` method.
