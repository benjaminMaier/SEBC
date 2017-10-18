### Check health of own files

```
[centos@ip-10-0-0-207 ~]$ hdfs fsck /user/centos/benjaminMaier/ -files -blocks
Connecting to namenode via http://ip-10-0-0-16.eu-west-1.compute.internal:50070
FSCK started by centos (auth:SIMPLE) from /10.0.0.207 for path /user/centos/benjaminMaier/ at Wed Oct 18 18:09:31 UTC 2017
/user/centos/benjaminMaier/ <dir>
/user/centos/benjaminMaier/_SUCCESS 0 bytes, 0 block(s):  OK

/user/centos/benjaminMaier/part-m-00000 262144000 bytes, 2 block(s):  OK
0. BP-1397609304-10.0.0.16-1508231919371:blk_1073742561_1737 len=134217728 Live_repl=3
1. BP-1397609304-10.0.0.16-1508231919371:blk_1073742563_1739 len=127926272 Live_repl=3

/user/centos/benjaminMaier/part-m-00001 262144000 bytes, 2 block(s):  OK
0. BP-1397609304-10.0.0.16-1508231919371:blk_1073742560_1736 len=134217728 Live_repl=3
1. BP-1397609304-10.0.0.16-1508231919371:blk_1073742562_1738 len=127926272 Live_repl=3

Status: HEALTHY
 Total size:    524288000 B
 Total dirs:    1
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 131072000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Wed Oct 18 18:09:31 UTC 2017 in 2 milliseconds


The filesystem under path '/user/centos/benjaminMaier/' is HEALTHY
```

### Check health of neighbour files

```
[centos@ip-10-0-0-207 ~]$ hdfs fsck /feanor21/input -files -blocks
Connecting to namenode via http://ip-10-0-0-16.eu-west-1.compute.internal:50070
FSCK started by centos (auth:SIMPLE) from /10.0.0.207 for path /feanor21/input at Wed Oct 18 18:11:02 UTC 2017
/feanor21/input <dir>
/feanor21/input/_SUCCESS 0 bytes, 0 block(s):  OK

/feanor21/input/part-m-00000 262144000 bytes, 2 block(s):  OK
0. BP-1397609304-10.0.0.16-1508231919371:blk_1073750794_9984 len=134217728 Live_repl=3
1. BP-1397609304-10.0.0.16-1508231919371:blk_1073750795_9985 len=127926272 Live_repl=3

/feanor21/input/part-m-00001 262144000 bytes, 2 block(s):  OK
0. BP-1397609304-10.0.0.16-1508231919371:blk_1073750796_9986 len=134217728 Live_repl=3
1. BP-1397609304-10.0.0.16-1508231919371:blk_1073750797_9987 len=127926272 Live_repl=3

Status: HEALTHY
 Total size:    524288000 B
 Total dirs:    1
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 131072000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Wed Oct 18 18:11:02 UTC 2017 in 2 milliseconds


The filesystem under path '/feanor21/input' is HEALTHY
```