---
title: How can I use rspec to test the JSON output of my controller in rails 3.0.11?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: You can use the `have\_http\_status` matcher to test that the response has the expected HTTP status code and use the `be\_json\_eql` matcher to test that the response body is valid JSON.
---

**Contents**

[TOC]

## Section 1: Setup

In order to test the JSON format of your controller in Rails 3.0.11, you will need to include the `rspec-rails` gem in your `Gemfile`:

```ruby
group :development, :test do
  gem 'rspec-rails', '~> 3.0'
end
```

Then, run `bundle install` to install the gem.

## Section 2: Generate RSpec Files

Once the gem is installed, you can generate the necessary RSpec files with the following command:

```
rails generate rspec:install
```

This will create the `spec` folder in your application and generate the necessary files and folders for testing with RSpec.

## Section 3: Write the Test

Next, you can write the test for your controller's JSON format. For example, if you have a `UsersController` that should return a JSON response with a list of users, you can write a test like this:

```ruby
require 'rails_helper'

RSpec.describe UsersController, type: :controller do
  describe "GET #index" do
    it "returns a list of users in JSON format" do
      get :index
      expect(response.body).to eq(User.all.to_json)
    end
  end
end
```

## Section 4: Run the Test

Finally, you can run the test with the following command:

```
rspec spec/controllers/users_controller_spec.rb
```

If the test passes, the JSON format of your controller is correct.
