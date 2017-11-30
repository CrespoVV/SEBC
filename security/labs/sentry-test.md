[root@ip-172-31-59-57 ec2-user]# su george
[george@ip-172-31-59-57 ec2-user]$ klist
Ticket cache: FILE:/tmp/krb5cc_1100
Default principal: george@RICOH.COM

Valid starting       Expires              Service principal
11/30/2017 00:46:07  12/01/2017 00:46:07  krbtgt/RICOH.COM@RICOH.COM
        renew until 12/07/2017 00:46:07
[george@ip-172-31-59-57 ec2-user]$ beeline
Beeline version 1.1.0-cdh5.12.1 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-59-57.ec2.internal@RICOH.COM
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-59-57.ec2.internal@RICOH.COM
Connected to: Apache Hive (version 1.1.0-cdh5.12.1)
Driver: Hive JDBC (version 1.1.0-cdh5.12.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20171130034343_5b11c6fd-0e6c-4957-bc15-5f60aa80caf0): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171130034343_5b11c6fd-0e6c-4957-bc15-5f60aa80caf0); Time taken: 0.075 seconds
INFO  : Executing command(queryId=hive_20171130034343_5b11c6fd-0e6c-4957-bc15-5f60aa80caf0): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171130034343_5b11c6fd-0e6c-4957-bc15-5f60aa80caf0); Time taken: 0.134 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_01  |
| sample_07  |
+------------+--+

[root@ip-172-31-59-57 ec2-user]# su ferdinand
[ferdinand@ip-172-31-59-57 ec2-user]$ klist
Ticket cache: FILE:/tmp/krb5cc_1200
Default principal: ferdinand@RICOH.COM

Valid starting       Expires              Service principal
11/30/2017 01:16:59  12/01/2017 01:16:59  krbtgt/RICOH.COM@RICOH.COM
        renew until 12/07/2017 01:16:59
[ferdinand@ip-172-31-59-57 ec2-user]$ beeline
Beeline version 1.1.0-cdh5.12.1 by Apache Hive
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-59-57.ec2.internal@RICOH.COM
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/ip-172-31-59-57.ec2.internal@RICOH.COM
Connected to: Apache Hive (version 1.1.0-cdh5.12.1)
Driver: Hive JDBC (version 1.1.0-cdh5.12.1)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20171130034444_a980cd9f-d03e-46e1-b14f-4c12195ebaa2): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171130034444_a980cd9f-d03e-46e1-b14f-4c12195ebaa2); Time taken: 0.067 seconds
INFO  : Executing command(queryId=hive_20171130034444_a980cd9f-d03e-46e1-b14f-4c12195ebaa2): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171130034444_a980cd9f-d03e-46e1-b14f-4c12195ebaa2); Time taken: 0.141 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.321 seconds)
