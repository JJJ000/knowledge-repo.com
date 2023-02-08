---
title: Convert MySQL results into JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: MySQL results can be encoded in JSON using the json\_encode() function.
---

**Contents**

[TOC]

1. Retrieve Data from MySQL Database
-----------------------------------

In order to encode MySQL results in Json, the first step is to retrieve the data from the MySQL database. This can be done using a SQL query, such as:

```sql
SELECT * FROM table_name;
```

This will return all the data from the specified table. 

2. Fetch Data into an Array
---------------------------

Once the data has been retrieved from the MySQL database, it needs to be fetched into an array. This can be done using a while loop, such as:

```php
$result = mysqli_query($conn, $sql);
 
$data = array();
while ($row = mysqli_fetch_assoc($result)) {
    $data[] = $row;
}
```

This will loop through the results and store them in an array. 

3. Encode Array into JSON
-------------------------

Once the data is stored in an array, it can be encoded into JSON. This can be done using the `json_encode` function, such as:

```php
$json = json_encode($data);
```

This will encode the array into a JSON string. 

4. Output JSON String
---------------------

Finally, the JSON string can be outputted. This can be done using the `echo` function, such as:

```php
echo $json;
```

This will output the JSON string to the browser.
