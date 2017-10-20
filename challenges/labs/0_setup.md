### Cloud provider

```
AWS
```

### Linux release: Centos 7 1602

```
[centos@ip-10-0-0-85 ~]$ cat /etc/redhat-release
CentOS Linux release 7.2.1511 (Core)
```

### Disk space on each node

```
[centos@ip-10-0-0-85 ~]$ df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/xvda1     xfs        50G  943M   50G   2% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.2G     0  7.2G   0% /dev/shm
tmpfs          tmpfs     7.2G   17M  7.2G   1% /run
tmpfs          tmpfs     7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvdb      ext3       37G   49M   35G   1% /mnt
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/0
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000


[centos@ip-10-0-0-166 ~]$ df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/xvda1     xfs        50G  943M   50G   2% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.2G     0  7.2G   0% /dev/shm
tmpfs          tmpfs     7.2G   17M  7.2G   1% /run
tmpfs          tmpfs     7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvdb      ext3       37G   49M   35G   1% /mnt
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/0
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000

[centos@ip-10-0-0-60 ~]$ df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/xvda1     xfs        50G  943M   50G   2% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.2G     0  7.2G   0% /dev/shm
tmpfs          tmpfs     7.2G   17M  7.2G   1% /run
tmpfs          tmpfs     7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvdb      ext3       37G   49M   35G   1% /mnt
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/0
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000

[centos@ip-10-0-0-188 ~]$ df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/xvda1     xfs        50G  943M   50G   2% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.2G     0  7.2G   0% /dev/shm
tmpfs          tmpfs     7.2G   17M  7.2G   1% /run
tmpfs          tmpfs     7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvdb      ext3       37G   49M   35G   1% /mnt
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/0
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000

[centos@ip-10-0-0-23 ~]$ df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/xvda1     xfs        50G  943M   50G   2% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.2G     0  7.2G   0% /dev/shm
tmpfs          tmpfs     7.2G   17M  7.2G   1% /run
tmpfs          tmpfs     7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvdb      ext3       37G   49M   35G   1% /mnt
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/0
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000
```

### yum repolist

```
[centos@ip-10-0-0-85 ~]$ yum repolist enabled
Loaded plugins: fastestmirror
Determining fastest mirrors
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                     repo name                      status
base/7/x86_64               CentOS-7 - Base                9,591
extras/7/x86_64             CentOS-7 - Extras                227
updates/7/x86_64            CentOS-7 - Updates               741
repolist: 10,559

[centos@ip-10-0-0-166 ~]$ yum repolist enabled
Loaded plugins: fastestmirror
Determining fastest mirrors
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                     repo name                      status
base/7/x86_64               CentOS-7 - Base                9,591
extras/7/x86_64             CentOS-7 - Extras                227
updates/7/x86_64            CentOS-7 - Updates               741
repolist: 10,559

[centos@ip-10-0-0-60 ~]$ yum repolist enabled
Loaded plugins: fastestmirror
Determining fastest mirrors
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                     repo name                      status
base/7/x86_64               CentOS-7 - Base                9,591
extras/7/x86_64             CentOS-7 - Extras                227
updates/7/x86_64            CentOS-7 - Updates               741
repolist: 10,559

[centos@ip-10-0-0-188 ~]$ yum repolist enabled
Loaded plugins: fastestmirror
Determining fastest mirrors
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                     repo name                      status
base/7/x86_64               CentOS-7 - Base                9,591
extras/7/x86_64             CentOS-7 - Extras                227
updates/7/x86_64            CentOS-7 - Updates               741
repolist: 10,559

[centos@ip-10-0-0-23 ~]$ yum repolist enabled
Loaded plugins: fastestmirror
Determining fastest mirrors
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                     repo name                      status
base/7/x86_64               CentOS-7 - Base                9,591
extras/7/x86_64             CentOS-7 - Extras                227
updates/7/x86_64            CentOS-7 - Updates               741
repolist: 10,559
```

### /etc/passwd for ernest and siwicki

```
[centos@ip-10-0-0-85 ~]$ cat /etc/passwd | grep ernest
ernest:x:2000:2000::/home/ernest:/bin/bash

[centos@ip-10-0-0-85 ~]$ cat /etc/passwd | grep siwicki
siwicki:x:3000:3000::/home/siwicki:/bin/bash
```

### /etc/group for usa and emea

```
[centos@ip-10-0-0-85 ~]$ cat /etc/group | grep usa
usa:x:3001:ernest

[centos@ip-10-0-0-85 ~]$ cat /etc/group | grep emea
emea:x:3002:siwicki
```