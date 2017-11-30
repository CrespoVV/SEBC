[crispin-dev@ip-172-31-49-75 jars]$ export HADOOP_USER_NAME=hdfs
[crispin-dev@ip-172-31-49-75 jars]$ hdfs dfs -mkdir /precious
[crispin-dev@ip-172-31-49-75 jars]$ hdfs dfs -ls /
Found 3 items
drwxr-xr-x   - hdfs supergroup          0 2017-11-28 21:56 /precious
drwxrwxrwt   - hdfs supergroup          0 2017-11-28 01:59 /tmp
drwxr-xr-x   - hdfs supergroup          0 2017-11-28 21:23 /user

[root@ip-172-31-49-75 home]# hdfs dfs -put SEBC-master.zip /precious
[root@ip-172-31-49-75 home]# hdfs dfs -la /precious
-la: Unknown command
[root@ip-172-31-49-75 home]# hdfs dfs -ls /precious
Found 1 items
-rw-r--r--   3 hdfs supergroup     474833 2017-11-28 22:18 /precious/SEBC-master.zip



[crispin-dev@ip-172-31-49-75 jars]$ hdfs dfsadmin -allowsnapshot /precious
Allowing snaphot on /precious succeeded

[root@ip-172-31-49-75 home]# hdfs dfs -createSnapshot /precious sebc-hdfs-test
Created snapshot /precious/.snapshot/sebc-hdfs-test


[root@ip-172-31-49-75 home]# hdfs dfs -rm -r /precious/SEBC-master.zip
17/11/28 22:24:03 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-49-75.ec2.internal:8020/precious/SEBC-master.zip' to trash at: hdfs://ip-172-31-49-75.ec2.internal:8020/user/hdfs/.Trash/Current/precious/SEBC-master.zip

[root@ip-172-31-49-75 home]# hdfs dfs -ls -R /precious/.snapshot
drwxr-xr-x   - hdfs supergroup          0 2017-11-28 22:23 /precious/.snapshot/sebc-hdfs-test
-rw-r--r--   3 hdfs supergroup     474833 2017-11-28 22:18 /precious/.snapshot/sebc-hdfs-test/SEBC-master.zip

[root@ip-172-31-49-75 home]# hdfs dfs -put /precious/.snapshot/sebc-hdfs-test/SEBC-master.zip /precious
