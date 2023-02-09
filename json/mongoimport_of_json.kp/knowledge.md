---
title: Importing a JSON file into mongodb
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Mongoimport is a command-line tool for importing data from a JSON file into a MongoDB database.
---

**Contents**

[TOC]

##Section 1 - Prerequisites

Before you can use mongoimport to import a JSON file, you must have a MongoDB database set up and running.

##Section 2 - Using Mongoimport

Once you have a MongoDB database set up and running, you can use mongoimport to import a JSON file. To do this, open a terminal window and navigate to the directory containing the JSON file. Then, type the following command:

`mongoimport --db <database_name> --collection <collection_name> --file <filename.json>`

Replace <database_name> with the name of the database you want to import the JSON file into, <collection_name> with the name of the collection you want to import the JSON file into, and <filename.json> with the name of the JSON file you want to import.

##Section 3 - Options

There are a few options you can use with mongoimport to customize the import. For example, you can use the --jsonArray option to import a JSON array instead of a single JSON document. You can also use the --drop option to drop the existing collection before importing the JSON file.

##Section 4 - Verifying the Import

Once you have imported the JSON file, you can verify that it was imported successfully by opening a MongoDB shell and running the db.collection.find() command. This will print out all of the documents in the collection you imported the JSON file into.
