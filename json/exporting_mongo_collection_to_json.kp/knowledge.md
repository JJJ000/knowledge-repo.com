---
title: Export a mongo collection as a JSON file
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: MongoDB provides the mongoexport utility to dump a collection into JSON format.
---

**Contents**

[TOC]

## Section 1: Export Collection

To export a MongoDB collection to a JSON file, use the mongoexport command. This command accepts the following parameters:

* `--host`: The MongoDB hostname or IP address.
* `--db`: The name of the MongoDB database.
* `--collection`: The name of the MongoDB collection.
* `--out`: The name of the output file.

For example, to export the “customers” collection from the “my_database” database to a JSON file named “customers.json”, run the following command:

```
mongoexport --host <hostname> --db my_database --collection customers --out customers.json
```

## Section 2: Import Collection

To import a JSON file into a MongoDB collection, use the mongoimport command. This command accepts the following parameters:

* `--host`: The MongoDB hostname or IP address.
* `--db`: The name of the MongoDB database.
* `--collection`: The name of the MongoDB collection.
* `--file`: The name of the input file.

For example, to import the “customers.json” file into the “my_database” database in the “customers” collection, run the following command:

```
mongoimport --host <hostname> --db my_database --collection customers --file customers.json
```

## Section 3: Format JSON

By default, mongoexport will export the collection in a JSON format with one document per line. To export the collection in a single JSON array, use the `--jsonArray` option.

For example, to export the “customers” collection from the “my_database” database to a JSON file named “customers.json” in an array format, run the following command:

```
mongoexport --host <hostname> --db my_database --collection customers --out customers.json --jsonArray
```

## Section 4: Pretty Print

By default, mongoexport will export the collection in a single line. To export the collection in a “pretty” format with indentation, use the `--pretty` option.

For example, to export the “customers” collection from the “my_database” database to a JSON file named “customers.json” in a pretty format, run the following command:

```
mongoexport --host <hostname> --db my_database --collection customers --out customers.json --pretty
```
