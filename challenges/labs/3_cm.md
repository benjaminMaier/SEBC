### hdfs dfs -ls /user

```
[centos@ip-10-0-0-85 java]$ hdfs dfs -ls /user
Found 6 items
drwxr-xr-x   - ernest  ernest           0 2017-10-20 08:58 /user/ernest
drwxrwxrwx   - mapred  hadoop           0 2017-10-20 08:55 /user/history
drwxrwxr-t   - hive    hive             0 2017-10-20 08:56 /user/hive
drwxrwxr-x   - hue     hue              0 2017-10-20 08:56 /user/hue
drwxrwxr-x   - oozie   oozie            0 2017-10-20 08:57 /user/oozie
drwxr-xr-x   - siwicki siwicki          0 2017-10-20 08:59 /user/siwicki
```

### CM API call

```
[centos@ip-10-0-0-166 java]$ curl -X GET -u admin:admin 'http://ec2-54-154-142-240.eu-west-1.compute.amazonaws.com:7180/api/v14/hosts'
{
  "items" : [ {
    "hostId" : "i-0ed0e4086b55e162c",
    "ipAddress" : "10.0.0.166",
    "hostname" : "ip-10-0-0-166.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-166.eu-west-1.compute.internal:7180/cmf/hostRedirect/i-0ed0e4086b55e162c",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332438016
  }, {
    "hostId" : "i-033d8017a84d27d36",
    "ipAddress" : "10.0.0.188",
    "hostname" : "ip-10-0-0-188.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-166.eu-west-1.compute.internal:7180/cmf/hostRedirect/i-033d8017a84d27d36",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332438016
  }, {
    "hostId" : "i-004d4a4ef7bea08ec",
    "ipAddress" : "10.0.0.23",
    "hostname" : "ip-10-0-0-23.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-166.eu-west-1.compute.internal:7180/cmf/hostRedirect/i-004d4a4ef7bea08ec",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332438016
  }, {
    "hostId" : "i-0356564022768140c",
    "ipAddress" : "10.0.0.60",
    "hostname" : "ip-10-0-0-60.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-166.eu-west-1.compute.internal:7180/cmf/hostRedirect/i-0356564022768140c",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332438016
  }, {
    "hostId" : "i-0f72318afb4684232",
    "ipAddress" : "10.0.0.85",
    "hostname" : "ip-10-0-0-85.eu-west-1.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-10-0-0-166.eu-west-1.compute.internal:7180/cmf/hostRedirect/i-0f72318afb4684232",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332438016
  } ]
}[
```

