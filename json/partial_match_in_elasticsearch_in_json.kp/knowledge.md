---
title: What is the syntax for performing a partial match in elasticsearch?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: You can use a wildcard or fuzzy query to do a partial match in Elasticsearch.
---

**Contents**

[TOC]

**Section 1: Create an Index**

To do a partial match in Elasticsearch, you must first create an index. An index is a collection of documents that have similar characteristics. You can create an index with the following command:

```
PUT /my_index
```

**Section 2: Add a Mapping**

Once you have created an index, you must add a mapping. A mapping is a definition of the fields and their types that will be stored in the index. You can add a mapping with the following command:

```
PUT /my_index/_mapping
{
  "properties": {
    "name": {
      "type": "text",
      "analyzer": "standard"
    }
  }
}
```

**Section 3: Index Documents**

Once you have created an index and added a mapping, you can index documents. Documents are the data that you want to store in the index. You can index documents with the following command:

```
POST /my_index/_doc
{
  "name": "John Doe"
}
```

**Section 4: Perform a Partial Match Query**

Once you have indexed documents, you can perform a partial match query. A partial match query is a query that matches documents that contain a specified string. You can perform a partial match query with the following command:

```
GET /my_index/_search
{
  "query": {
    "match": {
      "name": {
        "query": "Jo*",
        "operator": "and"
      }
    }
  }
}
```

This query will return all documents that contain a string that starts with "Jo", such as "John".
