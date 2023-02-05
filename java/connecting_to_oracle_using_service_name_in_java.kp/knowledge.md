---
title: How to connect to oracle using a service name instead of an sid
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can connect to Oracle using a Service Name instead of a SID in Java by using the OracleDataSource.setServiceName() method.
---

**Contents**

[TOC]

# Section 1: Prerequisites
- Oracle Database Installed
- Oracle Client Installed
- Oracle JDBC Driver Installed

# Section 2: Configuring tnsnames.ora
The tnsnames.ora file is an Oracle network configuration file that contains network service names mapped to connect descriptors for the local naming method.

The tnsnames.ora file is located in the Oracle Home directory.

```
<service_name> =
  (DESCRIPTION =
    (ADDRESS = (PROTOCOL = TCP)(HOST = <hostname>)(PORT = <port>))
    (CONNECT_DATA =
      (SERVER = DEDICATED)
      (SERVICE_NAME = <service_name>)
    )
  )
```

# Section 3: Establishing a Connection
Once the tnsnames.ora file is configured, you can use the service name to connect to the Oracle database.

```
String url = "jdbc:oracle:thin:@<service_name>";
Connection con = DriverManager.getConnection(url, user, password);
```

# Section 4: Troubleshooting
If you encounter any connection issues, you can use the Oracle Net Configuration Assistant to test the connection.
