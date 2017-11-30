##Start

```curl -X POST -u crispindev:Cloudera1! 'http://54.224.191.143:7180/api/v1/clusters/BCTestCluster/services/hive/commands/start'
{
  "id" : 2564,
  "name" : "Stop",
  "startTime" : "2017-11-30T17:31:38.205Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```

##Status

```
$ curl -u crispindev:Cloudera1! 'http://54.224.191.143:7180/api/v1/clusters/BCTestCluster/services/hive'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   445    0   445    0     0    445      0 --:--:-- --:--:-- --:--:--   749{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-54-226.ec2.internal:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STOPPED",
  "healthSummary" : "DISABLED",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "DISABLED"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "DISABLED"
  } ],
  "configStale" : false
}
```

##Start
```$ curl -X POST -u crispindev:Cloudera1! 'http://54.224.191.143:7180/api/v1/clusters/BCTestCluster/services/hive/commands/start'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   182    0   182    0     0    182      0 --:--:-- --:--:-- --:--:--   270{
  "id" : 2570,
  "name" : "Start",
  "startTime" : "2017-11-30T17:38:58.095Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}```




"serviceUrl" : "http://ip-172-31-54-226.ec2.internal:7180/cmf/serviceRedirect/oozie",
"serviceState" : "STARTED",
"healthSummary" : "GOOD",
"healthChecks" : [ {
  "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
  "summary" : "GOOD"
} ],
"configStale" : false
}, {
"name" : "hue",
"type" : "HUE",
"clusterRef" : {
  "clusterName" : "cluster"
},
"serviceUrl" : "http://ip-172-31-54-226.ec2.internal:7180/cmf/serviceRedirect/hue",
"serviceState" : "STARTED",
"healthSummary" : "GOOD",
"healthChecks" : [ {
  "name" : "HUE_HUE_SERVERS_HEALTHY",
  "summary" : "GOOD"
}, {
  "name" : "HUE_KT_RENEWERS_HEALTHY",
  "summary" : "GOOD"
}, {
  "name" : "HUE_LOAD_BALANCER_HEALTHY",
  "summary" : "GOOD"
} ],
"configStale" : false
}, {
"name" : "sentry",
"type" : "SENTRY",
"clusterRef" : {
  "clusterName" : "cluster"
},
"serviceUrl" : "http://ip-172-31-54-226.ec2.internal:7180/cmf/serviceRedirect/sentry",
"serviceState" : "STARTED",
"healthSummary" : "GOOD",
"healthChecks" : [ {
  "name" : "SENTRY_SENTRY_SERVERS_HEALTHY",
  "summary" : "GOOD"
} ],
"configStale" : false
} ]
}

Crispin.Velez@RICOHCO-1TPXRF2 MINGW32 ~ (master)
$ ^C

Crispin.Velez@RICOHCO-1TPXRF2 MINGW32 ~ (master)
$
