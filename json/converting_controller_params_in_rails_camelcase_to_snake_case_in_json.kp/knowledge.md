---
title: What would be the most effective method to change all controller parameters from camelcase to snake_case in rails?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use ActiveSupport`s #underscore method on the params hash.
---

**Contents**

[TOC]

## Introduction
In Rails, it is common to receive data from the client in camelCase format. However, the convention in Ruby and Rails is to use snake_case format. This can cause issues when trying to access or save data in the database. Therefore, it may be necessary to convert all controller params from camelCase to snake_case in Rails in Json. In this article, we will explore a few possible ways to accomplish this.

## First Approach: Use "Transform Keys"
One possible way to convert all controller params from camelCase to snake_case in Rails in Json is to use the "transform keys" method. This method is available in Ruby version 2.3 and higher. Here is an example of how to use it:

```ruby
# in your controller
def create
  snake_case_params = params.transform_keys { |key| key.underscore }
  # use snake_case_params to save or access data
end

# example params received in camelCase
params = { fooBar: 'baz' }

# output of transform_keys
snake_case_params = { foo_bar: 'baz' }
```

This approach directly converts keys from camelCase to snake_case, allowing for easy access to the parameters.

## Second Approach: Use A Controller Concern
Another way to convert all controller params from camelCase to snake_case in Rails in Json is to use a controller concern. A concern is a module that can be included in a controller to add additional methods or behavior. Here is an example of how to use a concern:

```ruby
# in your controller
class ApplicationController < ActionController::API
  include ParamConverter
end

# in your concern
module ParamConverter
  extend ActiveSupport::Concern

  included do
    before_action :convert_params
  end

  def convert_params
    params.deep_transform_keys!(&:underscore)
  end
end

# example params received in camelCase
params = { fooBar: 'baz' }

# output of deep_transform_keys
converted_params = { foo_bar: 'baz' }
```

This approach uses a concern to automatically convert all params to snake_case before any action is taken in the controller. This can be useful if you want to ensure consistency across all controller methods.

## Third Approach: Use A Middleware
A third possible way to convert all controller params from camelCase to snake_case in Rails in Json is to use a middleware. A middleware is a layer between the client and the Rails application that can modify the request or response. Here is an example of how to use a middleware:

```ruby
# in your middleware file
class SnakeCaseMiddleware
  def initialize(app)
    @app = app
  end

  def call(env)
    request = Rack::Request.new(env)
    request.params.deep_transform_keys!(&:underscore)
    @app.call(env)
  end
end

# in your application.rb or environment file
config.middleware.use SnakeCaseMiddleware
```

This approach uses a middleware to modify all requests before they reach the controller. This can be useful if you want to apply this transformation to all requests without modifying every controller.

## Conclusion
Converting all controller params from camelCase to snake_case in Rails in Json can be accomplished in a few different ways. The method you choose will depend on your specific use case and preferences, but the three approaches discussed in this article should provide a good starting point.
