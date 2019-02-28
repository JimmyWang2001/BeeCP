[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

Introduction
---
BeeCP,a lightweight and  fast JDBC connection pool implementation. 

<a href="http://central.maven.org/maven2/com/github/chris2018998/BeeCP/0.69/BeeCP-0.69.jar">Download beeCP_0.69.jar</a>

Configuration
---
|  Name  |   Description |   Remark |
| ------------ | ------------ | ------------ |
|  poolInitSize  | connection size need create when pool initialization  |   |
|  poolMaxSize |  max connnection size in pool |    |
|  borrowerMaxWaitTime |request timeout for  borrower  |   |
|  preparedStatementCacheSize | stement cache size |   |
| connectionIdleTimeout  | max idle time,then will be close  |    |
| connectionValidateSQL |  a test sql to check connection ative   |    |   |

 DataSource Demo
---
```java
String userId="root";
String password="";
String driver="com.mysql.jdbc.Driver";
String URL="jdbc:mysql://localhost/test";
BeeDataSourceConfig config = new JdbcPoolConfig(driver,URL,userId,password);
DataSource datasource = new BeeDataSource(config);
Connection con = datasource.getConnection();
....................
```
