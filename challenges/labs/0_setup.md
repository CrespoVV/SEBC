## <center> Cloud Provider

## Cloud Provider
AWS

## Intance IP and DNS

Cloudera Main DB
IP: 172.31.29.228 DNS: ip-172-31-29-228.ec2.internal

##Cloudera Manager Utilities

IP: 172.31.21.230 DNS: ip-172-31-21-230.ec2.internal

##Cloudera MN

IP: 172.31.19.106 DNS: ip-172-31-19-106.ec2.internal

##Cloudera WNs

1. IP: 172.31.23.153 DNS: ip-172-31-23-153.ec2.internal
2. IP: 172.31.19.81 DNS: ip-172-31-19-81.ec2.internal
3. IP: 172.31.31.23 DNS: ip-172-31-31-23.ec2.internal

## Linux Release
AMI ID
RHEL-7.4_HVM_GA-20170808-x86_64-2-Hourly2-GP2 (ami-c998b6b2)

## File Capacity
``` [ec2-user@ip-172-31-29-228 ~]$ lsblk
NAME    MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
xvda    202:0    0  80G  0 disk
├─xvda1 202:1    0   1M  0 part
└─xvda2 202:2    0  80G  0 part /
xvdb    202:16   0  80G  0 disk
```
File System
```[ec2-user@ip-172-31-29-228 ~]$ df
Filesystem     1K-blocks    Used Available Use% Mounted on
/dev/xvda2      83873772 1201332  82672440   2% /
devtmpfs        15337864       0  15337864   0% /dev
tmpfs           15358148       0  15358148   0% /dev/shm
tmpfs           15358148   16664  15341484   1% /run
tmpfs           15358148       0  15358148   0% /sys/fs/cgroup
tmpfs            3071632       0   3071632   0% /run/user/1000
```
## list /etc/passwd

```[root@ip-172-31-29-228 ec2-user]# cat /etc/passwd
saturn:x:2800:1002::/home/saturn:/bin/bash
haley:x:2900:1001::/home/haley:/bin/bash
```
```[root@ip-172-31-29-228 ec2-user]# cat /etc/group

comets:x:1001:
planets:x:1002:
```
