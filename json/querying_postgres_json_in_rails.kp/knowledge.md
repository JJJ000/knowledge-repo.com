---
title: How to query Postgres using the JSON data type in rails
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: You can query Postgres JSON data type in Rails using the ActiveRecord `where` method with `jsonb\_contains` operator.
---

**Contents**

[TOC]

1. Introduction
Postgres JSON data type is a powerful and versatile data type that allows developers to store and query JSON data in Rails applications. It provides a powerful set of features for storing and querying JSON data, including the ability to index fields, query with operators, and perform aggregations.

2. How to Use Postgres JSON in Rails
To use Postgres JSON data type in a Rails application, you will need to add the pg_json gem to your Gemfile. This gem provides a set of ActiveRecord methods for working with JSON data. After adding the gem, you can create a new model with a JSON column.

3. Querying JSON Data in Rails
Once you have your model set up, you can query the JSON data using the ActiveRecord methods provided by the pg_json gem. This includes methods such as `where_json`, `select_json`, and `order_json`. These methods allow you to query JSON data using the same syntax as you would use for querying regular columns.

4. Conclusion
Postgres JSON data type provides a powerful set of features for storing and querying JSON data in Rails applications. With the pg_json gem, you can easily query JSON data using the same syntax as you would use for querying regular columns. This makes it easy to work with JSON data in Rails applications.
