---
author: [Alfresco Documentation, Alfresco Documentation]
audience: 
category: [Installation, Alfresco Server]
keyword: [configuration files, solr]
---

# Database Configuration Properties

This topic describes properties that you can use to configure databases with Alfresco.

. Alfresco Enterprise supports Oracle, Microsoft SQL Server, DB2 as well MySQL and PostgreSQL. In addition, the Enterprise version can also be run against Ingres The following table lists and describes properties that you can use for database configuration

|Property name|Description|Default value|
|-------------|-----------|-------------|
|db.driver|The fully-qualified name of the JDBC driver class.|org.gjt.mm.mysql.Driver|
|db.url|The JDBC URL to the database connection.|jdbc:mysql:///$\{db.name\}|
|db.name|The database name.|alfresco|
|db.username|The name used for database authentication.|alfresco|
|db.password|The password used for database authentication.|alfresco|
|db.pool.statements.enable|A Boolean property. When set to `true` it indicates that all precompiled statements used on a connection will be kept open and cached for reuse.|true|
|db.pool.statements.max|The maximum number of precompiled statements to cache for each connection. The Alfresco default is 40. Note that Oracle does not allow more that 50 by default.|40|
|db.txn.isolation|The JDBC code number for the transaction isolation level, corresponding to those in the `java.sql.Connection` class. The value of -1 indicates that the database's default transaction isolation level should be used. For the Microsoft SQL Server JDBC driver, the special value of 4096 should be used to enable snapshot isolation.|-1|
|db.pool.initial|The number of connections opened when the pool is initialized.|10|
|db.pool.max|The maximum number of connections in the pool.|40|
|db.pool.idle|The maximum number of connections that are not in use kept open.|-1|
|db.pool.min|The minimum number of connections in the pool.|0|
|db.pool.wait.max|Time \(in milliseconds\) to wait for a connection to be returned before generating an exception when connections are unavailable. A value of 0 or -1 indicates that the exception should not be generated.|-1|
|db.pool.validate.query|The SQL query that will be used to ensure that your connections are still alive. This is useful if your database closes long-running connections after periods of inactivity.|This returns an empty string.|
|db.pool.validate.borrow|A Boolean property. When set to `true` it indicates that connections will be validated before being borrowed from the pool.|true|
|db.pool.validate.return|A Boolean property. When set to `true` it indicates that connections will be validated before being returned to the pool.|false|
|db.pool.evict.interval|Indicates the interval \(in milliseconds\) between eviction runs. If the value of this property is zero or less, idle objects will not be evicted in the background.|-1|
|db.pool.evict.idle.min|The minimum number of milliseconds that a connection may remain idle before it is eligible for eviction.|1800000|
|db.pool.evict.validate|A Boolean property. When set to `true` it indicates that the idle connections will be validated during eviction runs.|false|
|db.pool.abandoned.detect|A Boolean property. When set to `true` it indicates that a connection is considered abandoned and eligible for removal if it has been idle longer than the `db.pool.abandoned.time`.|false|
|db.pool.abandoned.time|The time in seconds before an abandoned connection can be removed.|300|

**Parent topic:**[Configuring the connection pool](../tasks/connpool-config.md)

