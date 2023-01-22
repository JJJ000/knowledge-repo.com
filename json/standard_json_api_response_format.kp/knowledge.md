---
title: What is the accepted format for JSON API responses?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-22 00:00:00
updated_at: 2023-01-22 00:00:00
tldr: The JSON API specification provides a standard format for JSON API responses.
---

**Contents**

[TOC]

### Overview

JSON API is a specification for how a client should request that resources be fetched or modified, and how a server should respond to those requests. It is designed to minimize both the number of requests and the amount of data transmitted between clients and servers. The JSON API response format defines the structure of a response to a request for a resource.

### Response Structure

The response should be a single JSON object, with the following structure:

```json
{
    "data": [
        {
            "type": "resourceType",
            "id": "resourceId",
            "attributes": {
                "attribute1": "value1",
                "attribute2": "value2"
            },
            "relationships": {
                "relatedResource": {
                    "data": {
                        "type": "relatedResourceType",
                        "id": "relatedResourceId"
                    }
                }
            }
        },
        {
            "type": "resourceType",
            "id": "resourceId2",
            "attributes": {
                "attribute1": "value1",
                "attribute2": "value2"
            },
            "relationships": {
                "relatedResource": {
                    "data": {
                        "type": "relatedResourceType",
                        "id": "relatedResourceId2"
                    }
                }
            }
        }
    ],
    "included": [
        {
            "type": "relatedResourceType",
            "id": "relatedResourceId",
            "attributes": {
                "attribute1": "value1",
                "attribute2": "value2"
            }
        },
        {
            "type": "relatedResourceType",
            "id": "relatedResourceId2",
            "attributes": {
                "attribute1": "value1",
                "attribute2": "value2"
            }
        }
    ]
}
```

### Response Properties

The response should have the following properties:

* `data`: An array of resource objects. Each object should have a `type`, `id`, `attributes`, and `relationships` property.
* `included` (optional): An array of related resource objects. Each object should have a `type`, `id`, and `attributes` property.
* `meta` (optional): A meta object containing non-standard meta-information about the response.
* `links` (optional): A links object containing links related to the response.

### Pagination

If the response is paginated, the response should include pagination information in the `meta` object. This should include the current page number, the total number of pages, and the total number of resources.
