### What is ubertask optimization?

ubertask optimization runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.

### Where in CM is the Kerberos Security Realm value displayed?

Administration -> Settings and filter for Kerberos on the left side

### Which CDH service(s) host a property for enabling Kerberos authentication?

No service enable this, because Kerberos enabling is done in Administration -> Security. So it´s a general property in Cloudera Manager

### How do you upgrade the CM agents?

Upgrade the Cloudera Manager Agent. You can use an upgrade wizard that is invoked when you connect to the Admin Console or manually install the Cloudera Manager Agent packages.

### Give the tsquery statement used to chart Hue's CPU utilization?

SELECT cpu_system_rate + cpu_user_rate WHERE serviceName = hue

### Name all the roles that make up the Hive service

HiveServer2, Hive Metastore Server and Hive Gateway

### What steps must be completed before integrating Cloudera Manager with Kerberos?

<ul>
<li>install kerberos libraries for kerberos server: krb5-server krb5-libs krb5-auth-dialog krb5-workstation</li>
<li>install kerberos libraries for kerberos clients: krb5-workstation krb5-libs krb5-auth-dialog</li>
<li>Add parameters max_life = 1d and max_renewable_life = 7d in /var/kerberos/krb5kdc/kdc.conf</li>
<li>Create the kerberos database</li>
<li>In kerberos Server, add cloudera-scm principal</li>
<li>Add */admin and cloudera-scm to ACL(Access Control List), which gives privilege to add principals for admin and cloudera-scm principal</li>
<li>Adds the password policy to the database</li>
<li>start kerberos</li>
</ul>

