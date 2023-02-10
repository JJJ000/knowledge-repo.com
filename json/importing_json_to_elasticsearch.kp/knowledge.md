---
title: Load a JSON file into elasticsearch
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The easiest way to import a JSON file into Elasticsearch is to use the Bulk API.
---

**Contents**

[TOC]

## Step 1: Create an Index

Before you can import a JSON file into Elasticsearch, you need to create an index. An index is a logical namespace which maps to one or more primary shards and can have zero or more replica shards.

To create an index, use the following command:

```
PUT my_index
{
  "mappings": {
    "my_type": {
      "properties": {
        "field_1": { "type": "text" },
        "field_2": { "type": "integer" }
      }
    }
  }
}
```

This command creates an index named `my_index` with two fields: `field_1` and `field_2`. These fields are of type `text` and `integer` respectively.

## Step 2: Upload the JSON File

Once the index is created, you can upload the JSON file to Elasticsearch. To do this, use the following command:

```
POST my_index/_doc/_bulk
{ "index": { "_id": 1 } }
{ "field_1": "value1", "field_2": 123 }
{ "index": { "_id": 2 } }
{ "field_1": "value2", "field_2": 456 }
```

This command uploads two documents to the `my_index` index. Each document contains two fields: `field_1` and `field_2`.

## Step 3: Refresh the Index

Once the documents have been uploaded, you need to refresh the index to make the changes visible. To refresh the index, use the following command:

```
POST my_index/_refresh
```

## Step 4: Query the Index

Finally, you can query the index to verify that the documents have been imported correctly. To query the index, use the following command:

```
GET my_index/_search
```

This command will return all the documents in the `my_index` index.
