### STOP Hive service

```
[centos@ip-10-0-0-207 ~]$ curl -X POST -u benjaminMaier:cloudera 'http://ec2-54-171-173-68.eu-west-1.compute.amazonaws.com:7180/api/v2/clusters/benjaminMaier/services/hive/commands/stop'
{
  "id" : 310,
  "name" : "Stop",
  "startTime" : "2017-10-18T09:04:45.709Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
```

### START Hive service

```
[centos@ip-10-0-0-207 ~]$curl -X POST -u benjaminMaier:cloudera 'http://ec2-54-171-173-68.eu-west-1.compute.amazonaws.com:7180/api/v2/clusters/benjaminMaier/services/hive/commands/start'
{
  "id" : 314,
  "name" : "Start",
  "startTime" : "2017-10-18T09:06:08.353Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}
```

### CHECK Hive service

```
[centos@ip-10-0-0-207 ~]$ curl -X GET -u benjaminMaier:cloudera 'http://ec2-54-171-173-68.eu-west-1.compute.amazonaws.com:7180/api/v2/clusters/benjaminMaier/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-10-0-0-207.eu-west-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD"
  } ],
  "configStale" : false,
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive"
}
```