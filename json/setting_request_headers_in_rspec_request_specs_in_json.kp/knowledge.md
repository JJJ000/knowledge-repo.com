---
title: What is the procedure for including request headers in an rspec request spec?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Include the header in the `headers` option when making the request.
---

**Contents**

[TOC]

1. Install RSpec Json Matchers 
   To set request headers in RSpec request spec in Json, first install the RSpec Json Matchers gem. This gem provides matchers for validating the response body of a request.

2. Configure RSpec
   Next, configure RSpec to use the RSpec Json Matchers gem. To do this, add the following line to the spec_helper.rb file:

```ruby
require 'rspec/json_matchers'
```

3. Set Request Headers
   Now, you can set the request headers in the request spec. For example, to set the “Content-Type” header to “application/json”, you can use the following code:

```ruby
headers = {
  'Content-Type': 'application/json'
}

get '/some_endpoint', headers: headers
```

4. Validate Response
   Finally, you can use the RSpec Json Matchers gem to validate the response body. For example, to check that the response body contains a certain key-value pair, you can use the following code:

```ruby
expect(response.body).to have_json_path('some_key')
expect(response.body).to have_json_type(String).at_path('some_key')
expect(response.body).to be_json_eql('some_value').at_path('some_key')
```
