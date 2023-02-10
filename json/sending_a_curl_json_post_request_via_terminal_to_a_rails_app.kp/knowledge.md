---
title: Make a curl post request with JSON data to a rails application in the terminal
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: curl -X POST -H `Content-Type application/json` -d `{`key``value`}` http//localhost3000/route
---

**Contents**

[TOC]

1. Setup cURL Request

```
curl -X POST -H "Content-Type: application/json" -d '{"name":"John Doe"}' http://localhost:3000/users
```

2. Configure Rails to Accept JSON Data

```ruby
# config/application.rb

module YourApp
  class Application < Rails::Application
    # ...
    config.middleware.use ActionDispatch::ParamsParser
    config.middleware.use ActionDispatch::Flash
    config.middleware.use ActionDispatch::Cookies
    config.middleware.use ActionDispatch::Session::CookieStore, {:key=>"_your_app_session"}
    config.middleware.use Rack::MethodOverride
    config.middleware.use ActionDispatch::Head
    config.middleware.use Rack::ConditionalGet
    config.middleware.use Rack::ETag
    config.middleware.insert_before ActionDispatch::Static, Rack::Rewrite
    config.middleware.insert_before 0, Rack::Cors do
      allow do
        origins '*'
        resource '*', :headers => :any, :methods => [:get, :post, :options, :delete, :put, :patch], :credentials => true
      end
    end
    config.middleware.use ActionDispatch::ParamsParser, {
      Mime::JSON => Proc.new { |raw_post|
        # Modified from action_dispatch/http/parameters.rb
        data = ActiveSupport::JSON.decode(raw_post)
        data = {:_json => data} unless data.is_a?(Hash)
        data.with_indifferent_access
      }
    }
  end
end
```

3. Create a Controller Action

```ruby
# app/controllers/users_controller.rb

class UsersController < ApplicationController
  def create
    user = User.new(user_params)
    if user.save
      render json: user, status: :created
    else
      render json: user.errors, status: :unprocessable_entity
    end
  end

  private

  def user_params
    params.require(:user).permit(:name)
  end
end
```

4. Test the Request

```
curl -X POST -H "Content-Type: application/json" -d '{"name":"John Doe"}' http://localhost:3000/users
```
