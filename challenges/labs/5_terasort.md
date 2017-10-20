### terasort as ernest

```
[ernest@ip-10-0-0-166 centos]$ kinit ernest
Password for ernest@BENJAMINMAIER.CO.UK:
[ernest@ip-10-0-0-166 centos]$ hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/ernest/tgen512m /user/ernest/terasort_output
17/10/20 10:11:19 INFO terasort.TeraSort: starting
17/10/20 10:11:20 INFO hdfs.DFSClient: Created token for ernest: HDFS_DELEGATION_TOKEN owner=ernest@BENJAMINMAIER.CO.UK, renewer=yarn, realUser=, issueDate=1508494280492, maxDate=1509099080492, sequenceNumber=11, masterKeyId=2 on 10.0.0.166:8020
17/10/20 10:11:20 INFO security.TokenCache: Got dt for hdfs://ip-10-0-0-166.eu-west-1.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.166:8020, Ident: (token for ernest: HDFS_DELEGATION_TOKEN owner=ernest@BENJAMINMAIER.CO.UK, renewer=yarn, realUser=, issueDate=1508494280492, maxDate=1509099080492, sequenceNumber=11, masterKeyId=2)
17/10/20 10:11:20 INFO input.FileInputFormat: Total input paths to process : 6
Spent 319ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 324ms
Sampling 10 splits of 156
Making 8 from 100000 sampled records
Computing parititions took 559ms
Spent 886ms computing partitions.
17/10/20 10:11:21 INFO client.RMProxy: Connecting to ResourceManager at ip-10-0-0-166.eu-west-1.compute.internal/10.0.0.166:8032
17/10/20 10:11:21 INFO mapreduce.JobSubmitter: number of splits:156
17/10/20 10:11:22 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1508492657672_0011
17/10/20 10:11:22 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.0.166:8020, Ident: (token for ernest: HDFS_DELEGATION_TOKEN owner=ernest@BENJAMINMAIER.CO.UK, renewer=yarn, realUser=, issueDate=1508494280492, maxDate=1509099080492, sequenceNumber=11, masterKeyId=2)
17/10/20 10:11:22 INFO impl.YarnClientImpl: Submitted application application_1508492657672_0011
17/10/20 10:11:22 INFO mapreduce.Job: The url to track the job: http://ip-10-0-0-166.eu-west-1.compute.internal:8088/proxy/application_1508492657672_0011/
17/10/20 10:11:22 INFO mapreduce.Job: Running job: job_1508492657672_0011
17/10/20 10:11:24 INFO mapreduce.Job: Job job_1508492657672_0011 running in uber mode : false
17/10/20 10:11:24 INFO mapreduce.Job:  map 0% reduce 0%
17/10/20 10:11:24 INFO mapreduce.Job: Job job_1508492657672_0011 failed with state FAILED due to: Application application_1508492657672_0011 failed 2 times due to AM Container for appattempt_1508492657672_0011_000002 exited with  exitCode: -1000
For more detailed output, check application tracking page:http://ip-10-0-0-166.eu-west-1.compute.internal:8088/proxy/application_1508492657672_0011/Then, click on links to logs of each attempt.
Diagnostics: Application application_1508492657672_0011 initialization failed (exitCode=1) with output: main : command provided 0
main : run as user is ernest
main : requested yarn user is ernest
Can't create directory /yarn/nm/usercache/ernest/appcache/application_1508492657672_0011 - Permission denied
java.io.FileNotFoundException: File file:/yarn/nm/usercache/ernest/appcache/application_1508492657672_0011 does not exist
        at org.apache.hadoop.fs.RawLocalFileSystem.deprecatedGetFileStatus(RawLocalFileSystem.java:590)
        at org.apache.hadoop.fs.RawLocalFileSystem.getFileLinkStatusInternal(RawLocalFileSystem.java:803)
        at org.apache.hadoop.fs.RawLocalFileSystem.getFileStatus(RawLocalFileSystem.java:580)
        at org.apache.hadoop.fs.FileSystem.primitiveMkdir(FileSystem.java:1066)
        at org.apache.hadoop.fs.DelegateToFileSystem.mkdir(DelegateToFileSystem.java:178)
        at org.apache.hadoop.fs.FilterFs.mkdir(FilterFs.java:205)
        at org.apache.hadoop.fs.FileContext$4.next(FileContext.java:735)
        at org.apache.hadoop.fs.FileContext$4.next(FileContext.java:731)
        at org.apache.hadoop.fs.FSLinkResolver.resolve(FSLinkResolver.java:90)
        at org.apache.hadoop.fs.FileContext.mkdir(FileContext.java:731)
        at org.apache.hadoop.yarn.server.nodemanager.containermanager.localizer.ContainerLocalizer.createDir(ContainerLocalizer.java:424)
        at org.apache.hadoop.yarn.server.nodemanager.containermanager.localizer.ContainerLocalizer.initDirs(ContainerLocalizer.java:416)
        at org.apache.hadoop.yarn.server.nodemanager.containermanager.localizer.ContainerLocalizer.runLocalization(ContainerLocalizer.java:130)
        at org.apache.hadoop.yarn.server.nodemanager.containermanager.localizer.ContainerLocalizer.main(ContainerLocalizer.java:383)

Failing this attempt. Failing the application.
17/10/20 10:11:24 INFO mapreduce.Job: Counters: 0
17/10/20 10:11:24 INFO terasort.TeraSort: done

```
