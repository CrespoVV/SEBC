## <center> CM Upgrade

API version

```$ curl -u crispindev:Cloudera1! http://54.224.191.143:7180/api/version
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100     3  100     3    0     0      3      0  0:00:01 --:--:--  0:00:01     6v18
````

CM version


```$ curl -u crispindev:Cloudera1! http://54.224.191.143:7180/api/v18/cm/version
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   171    0   171    0     0    171      0 --:--:-- --:--:-- --:--:--   377{
  "version" : "5.13.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20171002-1719",
  "gitHash" : "bd657e597e6743c458ee2c9aabe808b7c972981c",
  "snapshot" : false
}
```

List CM users

```$ curl -u crispindev:Cloudera1! http://54.224.191.143:7180/api/v18/users
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   216    0   216    0     0    216      0 --:--:-- --:--:-- --:--:--   553{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "crispindev",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ]
  } ]
}
```
Databse Server by CM
```$ curl -u crispindev:Cloudera1! http://54.224.191.143:7180/api/v18/cm/scmDbInfo
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100    55    0    55    0     0     55      0 --:--:-- --:--:-- --:--:--   125{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```
