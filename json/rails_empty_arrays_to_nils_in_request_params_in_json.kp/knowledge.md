---
title: In the parameters of the request, rails will change empty arrays into nil values
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: No, Rails does not convert empty arrays into nils in params of the request in Json.
---

**Contents**

[TOC]

**Yes**

**How Rails Converts Empty Arrays**

Rails converts empty arrays into nil when it processes the params of the request in JSON. This is done by the `ActiveSupport::JSON.decode` method which is called when a request is made. This method takes the params and decodes them into a Ruby hash. If the param is an empty array, it will be converted to nil.

**Why Rails Converts Empty Arrays**

Rails converts empty arrays to nil because it is a more consistent way of handling data. This allows for better data validation and prevents unexpected values from being passed in. It also makes it easier to write code that deals with empty arrays, as nil is a simpler value to work with.

**Alternatives**

If you don't want your empty arrays to be converted to nil, you can use the `ActiveSupport::JSON.encode` method to encode the params before sending them. This will ensure that the empty arrays are sent as empty arrays instead of nil.
