---
title: When rendering JSON in rails, make sure to incorporate the linked model
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: You can include associated model data in the rendered JSON response in Rails using the `include` option in the `render json` method.
---

**Contents**

[TOC]

## Introduction
In Rails, rendering JSON is a very common task that often involves associations between models. JSON representation of Active Record models is usually required when you need to exchange data between the front-end and back-end. To include associated models when rendering JSON in Rails, you need to follow some standard practices. This article will guide you through the necessary steps you need to follow to include JSON representation of associated models in your Rails application.

## Section 1: Define your association
Firstly, you need to define the association between the two models by specifying the `belongs_to` and `has_many` associations in the Active Record models. For example, let's say you have two models - `Author` and `Book`. The `Author` model has many `Book` models, and a `Book` model belongs to an `Author`. Therefore, you will define the association between the `Author` and `Book` models as shown below:

```ruby
class Author < ApplicationRecord
  has_many :books
end

class Book < ApplicationRecord
  belongs_to :author
end
```

## Section 2: Use the `includes` method
Once the association between the models is defined, you can use the `includes` method to include the associated models in your JSON response. The `includes` method helps you to avoid the N+1 query problem. You just need to add it to your controller action as shown below:

```ruby
class BooksController < ApplicationController
  def index
    @books = Book.includes(:author)
    render json: @books.to_json(:include => :author)
  end
end
```

In the above example, we are including the `author` model in the `books` JSON response using the `includes` method. The `to_json` method is used to convert the `@books` object to JSON. 

## Section 3: Use the `as_json` method
Another way to include associated models in your JSON response is by using the `as_json` method. You can override the `as_json` method in your models and specify which associations to include. For example, let's say you want to include the `author` model in the JSON response for the `Book` model. You can provide an implementation for the `as_json` method as shown below:

```ruby
class Book < ApplicationRecord
  belongs_to :author

  def as_json(options={})
    super(options.merge(include: :author))
  end
end
```

In the above example, we are overriding the `as_json` method of the `Book` model to include the `author` model in the JSON response.


## Conclusion
By following the above steps, you can easily include associated models in your JSON response in Rails. You can use either the `includes` method or override the `as_json` method to achieve the same result. Including associated models in your JSON response can help improve the performance of your application by avoiding the N+1 query problem.
