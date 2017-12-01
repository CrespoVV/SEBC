## <center> System Configuration checks

Check Swappiness

```[root@ip-172-31-49-75 ec2-user]# cat /proc/sys/vm/swappiness
10
```

Check disk Mounts

```AME    MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
xvda    202:0    0  80G  0 disk
├─xvda1 202:1    0   1M  0 part
└─xvda2 202:2    0  80G  0 part /
xvdb    202:16   0  80G  0 disk /data

Filesystem volume name:   <none>
Last mounted on:          /data
Filesystem UUID:          ca4ed200-bb14-4b3b-8aca-5dc194087800
Filesystem magic number:  0xEF53
Filesystem revision #:    1 (dynamic)
Filesystem features:      has_journal ext_attr resize_inode dir_index filetype needs_recovery extent 64bit flex_bg sparse_super large_file huge_file uninit_bg dir_nlink extra_isize
Filesystem flags:         signed_directory_hash
Default mount options:    user_xattr acl
Filesystem state:         clean
Errors behavior:          Continue
Filesystem OS type:       Linux
Inode count:              5242880
Block count:              20971520
Reserved block count:     1048576
Free blocks:              20595296
Free inodes:              5242869
First block:              0
Block size:               4096
Fragment size:            4096
Group descriptor size:    64
Reserved GDT blocks:      1024
Blocks per group:         32768
Fragments per group:      32768
Inodes per group:         8192
Inode blocks per group:   512
Flex block group size:    16
Filesystem created:       Tue Nov 28 01:37:47 2017
Last mount time:          Tue Nov 28 01:42:28 2017
Last write time:          Tue Nov 28 01:42:28 2017
Mount count:              1
Maximum mount count:      -1
Last checked:             Tue Nov 28 01:37:47 2017
Check interval:           0 (<none>)
Lifetime writes:          132 MB
Reserved blocks uid:      0 (user root)
Reserved blocks gid:      0 (group root)
First inode:              11
Inode size:               256
Required extra isize:     28
Desired extra isize:      28
Journal inode:            8
Default directory hash:   half_md4
Directory Hash Seed:      85293440-be81-4199-98a0-7e83df7257c6
Journal backup:           inode blocks

[root@ip-172-31-49-75 ec2-user]# sudo file -s /dev/xvda2
/dev/xvda2: SGI XFS filesystem data (blksz 4096, inosz 512, v2 dirs)
```
Diable Hugepage Support

```
echo never > /sys/kernel/mm/transparent_hugepage/enabled
echo never > /sys/kernel/mm/transparent_hugepage/defrag

[root@ip-172-31-49-75 ec2-user]# sudo chmod a+x /etc/rc.d/rc.local && sudo
/etc/rc.d/rc.local
```

Network Interface Config

```[root@ip-172-31-49-75 ec2-user]# ifconfig -a
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.49.75  netmask 255.255.240.0  broadcast 172.31.63.255
        inet6 fe80::1080:e3ff:fe56:53c  prefixlen 64  scopeid 0x20<link>
        ether 12:80:e3:56:05:3c  txqueuelen 1000  (Ethernet)
        RX packets 3793169  bytes 3760722677 (3.5 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 2389786  bytes 2230785411 (2.0 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
        lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1  (Local Loopback)
        RX packets 739226  bytes 1478321534 (1.3 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 739226  bytes 1478321534 (1.3 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```
Check Local Host lookups
```[ec2-user@ip-172-31-61-22 home]$ nslookup ip-172-31-61-22.ec2.internal
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
Name:   ip-172-31-61-22.ec2.internal
Address: 172.31.61.22

[ec2-user@ip-172-31-61-22 home]$ nslookup 172.31.61.22
Server:         172.31.0.2
Address:        172.31.0.2#53

Non-authoritative answer:
22.61.31.172.in-addr.arpa       name = ip-172-31-61-22.ec2.internal.

Authoritative answers can be found from:
```
NSCD service running:

```[root@ip-172-31-49-75 etc]# service nscd status
Redirecting to /bin/systemctl status nscd.service
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Wed 2017-11-29 03:55:36 UTC; 5s ago
  Process: 25405 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 25406 (nscd)
   CGroup: /system.slice/nscd.service
           └─25406 /usr/sbin/nscd
```

NTPD Service running:

```[root@ip-172-31-49-75 etc]# service ntpd status
           Redirecting to /bin/systemctl status ntpd.service
           ● ntpd.service - Network Time Service
              Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
              Active: active (running) since Wed 2017-11-29 04:00:08 UTC; 5s ago
             Process: 26000 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
            Main PID: 26001 (ntpd)
              CGroup: /system.slice/ntpd.service
                      └─26001 /usr/sbin/ntpd -u ntp:ntp -g
```
