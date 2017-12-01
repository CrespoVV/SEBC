## Check DB Server Hostname

mysql> slect @@hostname hostname;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'slect @@hostname hostname' at line 1
mysql> select @@hostname hostname;
+-------------------------------+
| hostname                      |
+-------------------------------+
| ip-172-31-21-230.ec2.internal |
+-------------------------------+
1 row in set (0.00 sec)


##Database version

mysql> SHOW VARIABLES LIKE "%version%";
+-------------------------+------------------------------+
| Variable_name           | Value                        |
+-------------------------+------------------------------+
| innodb_version          | 5.7.20                       |
| protocol_version        | 10                           |
| slave_type_conversions  |                              |
| tls_version             | TLSv1,TLSv1.1                |
| version                 | 5.7.20                       |
| version_comment         | MySQL Community Server (GPL) |
| version_compile_machine | x86_64                       |
| version_compile_os      | Linux                        |
+-------------------------+------------------------------+
8 rows in set (0.00 sec)


## show databases

mysql> show databses;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'databses' at line 1
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| activitym          |
| clouderanas        |
| clouderanms        |
| hue                |
| metastore          |
| mysql              |
| oozie              |
| performance_schema |
| reportm            |
| scm                |
| sentrys            |
| sqoop              |
| sys                |
+--------------------+
14 rows in set (0.00 sec)
