---
title: How can I export the schema of a bigquery table as json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Yes, you can use the BigQuery API to export a BigQuery table`s schema as JSON.
---

**Contents**

[TOC]

### Using the BigQuery Web UI
1. Navigate to the BigQuery web UI and open the table you would like to export the schema for. 
2. Click the "More" dropdown menu and select "Export Table". 
3. Under "Export Format", select "JSON". 
4. Click the "Export" button. 

### Using the BigQuery Command Line Tool
1. Install the BigQuery command line tool. 
2. Run the following command to export the table's schema as JSON: 
```
bq show --format=prettyjson <dataset_name>.<table_name>
```
3. The command will output the table's schema in JSON format.
