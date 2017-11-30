YARN Map Reduce Job.

Run 1


Map 8 Reduce 1 Container Memory 512 1024


[root@ip-172-31-61-22 crispindev]# nano YARNtest.sh
[root@ip-172-31-61-22 crispindev]# su crispindev
[crispindev@ip-172-31-61-22 ~]$ ./YARNtest.sh
Testing loop started on Thu Nov 30 22:46:36 UTC 2017

real    1m33.693s
user    0m5.691s
sys     0m0.308s

real    2m35.022s
user    0m8.264s
sys     0m0.381s
Deleted /user/crispindev/tg-10GB-8-1-512
Deleted /user/crispindev/ts-10GB-8-1-512

real    1m28.049s
user    0m5.495s
sys     0m0.315s

real    2m21.560s
user    0m7.599s
sys     0m0.364s
Deleted /user/crispindev/tg-10GB-8-1-1024
Deleted /user/crispindev/ts-10GB-8-1-1024
Testing loop ended on Thu Nov 30 22:54:45 UTC 2017
[crispindev@ip-172-31-61-22 ~]$
[crispindev@ip-172-31-61-22 ~]$ exit
exit


Run 2

Map 8 Reduce 1 Container Memory 512 1024

[root@ip-172-31-61-22 crispindev]# nano YARNtest.sh
[root@ip-172-31-61-22 crispindev]# su crispindev
[crispindev@ip-172-31-61-22 ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_1201
Default principal: crispindev@RICOH.COM

Valid starting       Expires              Service principal
11/30/2017 17:11:24  12/01/2017 17:11:24  krbtgt/RICOH.COM@RICOH.COM
        renew until 12/07/2017 17:11:24
[crispindev@ip-172-31-61-22 ~]$ ./YARNtest.sh
Testing loop started on Thu Nov 30 23:11:24 UTC 2017

real    1m37.049s
user    0m5.719s
sys     0m0.312s

real    1m40.811s
user    0m7.640s
sys     0m0.339s
Deleted /user/crispindev/tg-10GB-12-4-1024
Deleted /user/crispindev/ts-10GB-12-4-1024

real    1m34.638s
user    0m5.520s
sys     0m0.332s

real    1m45.267s
user    0m7.388s
sys     0m0.371s
Deleted /user/crispindev/tg-10GB-12-4-2048
Deleted /user/crispindev/ts-10GB-12-4-2048
Testing loop ended on Thu Nov 30 23:18:13 UTC 2017
