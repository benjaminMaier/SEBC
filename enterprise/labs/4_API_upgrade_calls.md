
### Report the latest available version of the API

```
[centos@ip-10-0-0-207 ~]$ curl -X GET -u benjaminMaier:cloudera 'http://ec2-54-171-173-68.eu-west-1.compute.amazonaws.com:7180/api/version'
v14
```


### Report the CM version

```
[centos@ip-10-0-0-207 ~]$ curl -X GET -u benjaminMaier:cloudera 'http://ec2-54-171-173-68.eu-west-1.compute.amazonaws.com:7180/api/v14/cm/version'
{
  "version" : "5.9.3",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170627-1506",
  "gitHash" : "23506bb4e114dd460bdac64c57a672e6be631907",
  "snapshot" : false
}
```

### List all CM users

```
[centos@ip-10-0-0-207 ~]$ curl -X GET -u benjaminMaier:cloudera 'http://ec2-54-171-173-68.eu-west-1.compute.amazonaws.com:7180/api/v14/users'
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "benjaminMaier",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}
```

### Report the database server in use by CM

```
[centos@ip-10-0-0-207 ~]$ curl -X GET -u benjaminMaier:cloudera 'http://ec2-54-171-173-68.eu-west-1.compute.amazonaws.com:7180/api/v14/cm/scmDbInfo'
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```