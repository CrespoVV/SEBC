## <center> CM Monitoring Lab


* What is ubertask optimization?

It is a property part of the Gateway Default Group Role and it is used to tune performance of the different mapreduce Jobs.
When enabled it runs sufficiently small jobs sequentially within a single JVM.

Ubertask Maximum Job Size.
Threshold for number of input bytes beyond a job is considered too big.
Ubertask Maximum Reduces.
Threshold for numer of maps beyond which a job is connsidered to big for optimization.
Ubertask Maximum Reduces.
Threshold for number of reduces beyond which a job is considered too big for optimization.

* Where in CM is the Kerberos Security Realm value displayed?

Where is Kerberso Security Realm in CM?
Administration->Settings on the left Kerberos

Kerberos Security Realm->
default_realm

* Which CDH service(s) host a property for enabling Kerberos authentication?
Hue
Hive
HDFS
YARN
Sentry
Impala
Zookeper

* How do you upgrade the CM agents?
[Procedure to upgrade CM Agents](https://www.cloudera.com/documentation/enterprise/5-6-x/topics/cm_ag_upgrade_cm5.html#cmig_topic_9_4_5)

* Give the `tsquery` statement used to chart Hue's CPU utilization?

``SELECT cpu_user_rate / getHostFact(numCores, 1) * 100 WHERE entityName = "hue-HUE_SERVER-2fea9a9a9405a2b2a94593ed67306cff" AND category = ROLE``

* Name all the roles that make up the Hive service
There are two Hive service roles:
Hive Metastore Server. This role manages the Metastore process when Hive is configured with a Remote Metastore. You are strongly encouraged to read Configuring the Hive Metastore (CDH 4) or Configuring the Hive Metastore (CDH 5).
HiveServer2 - supports a Thrift API tailored for JDBC and ODBC clients, Kerberos authentication, and multi-client concurrency. There is also a CLI for HiveServer2 named Beeline. Cloudera recommends that you deploy HiveServer2 whenever possible. You can use the original HiveServer, and run it concurrently with HiveServer2. However, Cloudera Manager does not manage HiveServer, so you must configure and manage it outside Cloudera Manager. See HiveServer2 documentation (CDH 4) or HiveServer2 documentation (CDH 5) for more information.

* What steps must be completed before integrating Cloudera Manager with Kerberos?

Asuming CM and CDH are already installed:

Step 1.

Create an admin user across all hosts.
Install packages for a Kerberos server on a host : KDC and Kerberos Server.
Install package for kerberos client on every host: host1, host2, host3....
```yum -y install krb5-server krb5-libs krb5-auth-dialog krb5-workstation
yum -y install krb5-workstation krb5-libs krb5-auth-dialog```

Step 2.
Modify the following files in the KDC and KRB server host to add REALM and parameters for max life and renewable tickets:
```/var/kerberos/krb5kdc/kdc.conf
/etc/krb5.conf```

Step 3.
Modify the conf file in every client adjusting Realm, KDC server Host, tkt and tgs encryption:
`/etc/krb5.conf`

Step 4.
Create the database using the kdb5_util utility. (Server)
```/usr/sbin/kdb5_util create -s```

Step 5
add cloudera-scm principal.
```kadmin.local
kadmin.local:  addprinc cloudera-scm@RICOH.COM```

Step 6
Add */admin*/ and cloudera-scm to ACL(Access Control List), which gives privilege to add principals for admin and cloudera-scm principal.

```vim /var/kerberos/krb5kdc/kadm5.acl
*/admin@PUNEETHA.COM *
cloudera-scm@PUNEETHA.COM admilc```

Step 7
Add password policy
```kadmin.local
kadmin.local:  addpol admin
kadmin.local:  addpol users
kadmin.local:  addpol hosts
kadmin.local:  exit```

Step 8
Start Kerberos
```service krb5kdc start
service kadmin start```
