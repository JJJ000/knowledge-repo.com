---
title: How can you use a view to render JSON in rails?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: In Rails, you can render JSON using a view by using the `render json` method.
---

**Contents**

[TOC]

1. Setup

Make sure you have the `jbuilder` gem added to your Gemfile and run `bundle install`.

2. Create the View

Create a view file in `app/views/` with a `.json.jbuilder` extension. For example, if you wanted to create a view for a `Book` model, you would create a `app/views/books/show.json.jbuilder` file.

3. Write the View

In the view, you can use the `json` helper to create a JSON object. For example, if you wanted to render a `Book` model, you could write something like this:

```ruby
json.title @book.title
json.author @book.author
```

4. Render the View

In your controller action, you can render the view using the `render` method. For example, if your `Book` controller has a `show` action, you could render the view using something like this:

```ruby
render :show
```
