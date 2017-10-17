########CM Install Lab#######

###swappiness###
[benjaminMaier@ip-10-0-0-207 centos]$ cat /proc/sys/vm/swappiness
1

[centos@ip-10-0-0-60 ~]$ cat /proc/sys/vm/swappiness
1

[centos@ip-10-0-0-211 ~]$ sudo sysctl vm.swappiness=1
vm.swappiness = 1
[centos@ip-10-0-0-211 ~]$ cat /proc/sys/vm/swappiness
1

[centos@ip-10-0-0-54 ~]$ cat /proc/sys/vm/swappiness
1

[centos@ip-10-0-0-16 ~]$ cat /proc/sys/vm/swappiness
1

[centos@ip-10-0-0-250 ~]$ cat /proc/sys/vm/swappiness
1




###reserve space
[benjaminMaier@ip-10-0-0-207 centos]$ df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/xvda1     xfs        40G   17G   24G  43% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.2G     0  7.2G   0% /dev/shm
tmpfs          tmpfs     7.2G   25M  7.2G   1% /run
tmpfs          tmpfs     7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvdb      ext3       37G  9.0G   26G  26% /mnt
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/995
/dev/xvdc      ext3       37G  8.9G   27G  26% /data0
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/0
cm_processes   tmpfs     7.2G  2.0M  7.2G   1% /run/cloudera-scm-agent/process


[centos@ip-10-0-0-60 ~]$ df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/xvda1     xfs        40G   17G   24G  42% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.2G     0  7.2G   0% /dev/shm
tmpfs          tmpfs     7.2G   25M  7.2G   1% /run
tmpfs          tmpfs     7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvdb      ext3       37G   10G   25G  29% /mnt
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/0
/dev/xvdc      ext3       37G   11G   25G  30% /data0
cm_processes   tmpfs     7.2G  1.2M  7.2G   1% /run/cloudera-scm-agent/process


[centos@ip-10-0-0-54 ~]$ df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/xvda1     xfs        40G   16G   25G  39% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.2G     0  7.2G   0% /dev/shm
tmpfs          tmpfs     7.2G   25M  7.2G   1% /run
tmpfs          tmpfs     7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvdb      ext3       37G  9.4G   26G  27% /mnt
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/0
/dev/xvdc      ext3       37G  9.2G   26G  27% /data0
cm_processes   tmpfs     7.2G  1.4M  7.2G   1% /run/cloudera-scm-agent/process


[centos@ip-10-0-0-16 ~]$ df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/xvda1     xfs        40G  6.8G   34G  17% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.2G     0  7.2G   0% /dev/shm
tmpfs          tmpfs     7.2G   25M  7.2G   1% /run
tmpfs          tmpfs     7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvdb      ext3       37G   49M   35G   1% /mnt
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/0
/dev/xvdc      ext3       37G   52M   35G   1% /data0
cm_processes   tmpfs     7.2G   19M  7.2G   1% /run/cloudera-scm-agent/process


[centos@ip-10-0-0-250 ~]$ df -hT
Filesystem     Type      Size  Used Avail Use% Mounted on
/dev/xvda1     xfs        40G   18G   23G  44% /
devtmpfs       devtmpfs  7.3G     0  7.3G   0% /dev
tmpfs          tmpfs     7.2G     0  7.2G   0% /dev/shm
tmpfs          tmpfs     7.2G   25M  7.2G   1% /run
tmpfs          tmpfs     7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvdb      ext3       37G   12G   24G  34% /mnt
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/1000
tmpfs          tmpfs     1.5G     0  1.5G   0% /run/user/0
/dev/xvdc      ext3       37G   12G   24G  33% /data0
cm_processes   tmpfs     7.2G  1.5M  7.2G   1% /run/cloudera-scm-agent/process



###Disable transparent hugepage support
[benjaminMaier@ip-10-0-0-207 centos]$ cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never

[centos@ip-10-0-0-60 ~]$ cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never

[centos@ip-10-0-0-54 ~]$ cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never

[centos@ip-10-0-0-16 ~]$ cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never

[centos@ip-10-0-0-250 ~]$ cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never


###Network interface configuaration
[benjaminMaier@ip-10-0-0-207 centos]$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 10.0.0.207  netmask 255.255.255.0  broadcast 10.0.0.255
        inet6 fe80::886:c9ff:fed5:2744  prefixlen 64  scopeid 0x20<link>
        ether 0a:86:c9:d5:27:44  txqueuelen 1000  (Ethernet)
        RX packets 11077518  bytes 42808011233 (39.8 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 6076678  bytes 43484260519 (40.4 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 0  (Local Loopback)
        RX packets 2565913  bytes 36892126881 (34.3 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 2565913  bytes 36892126881 (34.3 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[centos@ip-10-0-0-60 ~]$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 10.0.0.60  netmask 255.255.255.0  broadcast 10.0.0.255
        inet6 fe80::8b6:bdff:feff:9e76  prefixlen 64  scopeid 0x20<link>
        ether 0a:b6:bd:ff:9e:76  txqueuelen 1000  (Ethernet)
        RX packets 9904970  bytes 45894941009 (42.7 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 4947710  bytes 38439727030 (35.7 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 0  (Local Loopback)
        RX packets 3187426  bytes 66607187700 (62.0 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 3187426  bytes 66607187700 (62.0 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[centos@ip-10-0-0-54 ~]$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 10.0.0.54  netmask 255.255.255.0  broadcast 10.0.0.255
        inet6 fe80::87c:fbff:fed4:54bc  prefixlen 64  scopeid 0x20<link>
        ether 0a:7c:fb:d4:54:bc  txqueuelen 1000  (Ethernet)
        RX packets 9454272  bytes 40287924512 (37.5 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 4865118  bytes 44569001568 (41.5 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 0  (Local Loopback)
        RX packets 2275971  bytes 45576296538 (42.4 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 2275971  bytes 45576296538 (42.4 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[centos@ip-10-0-0-16 ~]$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 10.0.0.16  netmask 255.255.255.0  broadcast 10.0.0.255
        inet6 fe80::80d:b6ff:fec8:b46e  prefixlen 64  scopeid 0x20<link>
        ether 0a:0d:b6:c8:b4:6e  txqueuelen 1000  (Ethernet)
        RX packets 3389157  bytes 3780588269 (3.5 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 2432576  bytes 2248988059 (2.0 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 0  (Local Loopback)
        RX packets 431900  bytes 478561766 (456.3 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 431900  bytes 478561766 (456.3 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

[centos@ip-10-0-0-250 ~]$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 10.0.0.250  netmask 255.255.255.0  broadcast 10.0.0.255
        inet6 fe80::80f:afff:fe0e:d93a  prefixlen 64  scopeid 0x20<link>
        ether 0a:0f:af:0e:d9:3a  txqueuelen 1000  (Ethernet)
        RX packets 9281629  bytes 46795709738 (43.5 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 5526693  bytes 40468657458 (37.6 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 0  (Local Loopback)
        RX packets 2340412  bytes 46887141825 (43.6 GiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 2340412  bytes 46887141825 (43.6 GiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0


 
		  
###forward and reverse host lookups
[centos@ip-10-0-0-207 ~]$ getent hosts `hostname`
10.0.0.207      ip-10-0-0-207.eu-west-1.compute.internal


[centos@ip-10-0-0-60 ~]$ getent hosts `hostname`
10.0.0.60       ip-10-0-0-60.eu-west-1.compute.internal

[centos@ip-10-0-0-54 ~]$ getent hosts `hostname`
10.0.0.54       ip-10-0-0-54.eu-west-1.compute.internal

[centos@ip-10-0-0-16 ~]$ getent hosts `hostname`
10.0.0.16       ip-10-0-0-16.eu-west-1.compute.internal

[centos@ip-10-0-0-250 ~]$ getent hosts `hostname`
10.0.0.250      ip-10-0-0-250.eu-west-1.compute.internal



###nscd service is running
sudo yum install nscd -y

[centos@ip-10-0-0-207 ~]$ sudo systemctl status nscd
? nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-10-17 08:24:28 UTC; 7h ago
 Main PID: 16470 (nscd)
   CGroup: /system.slice/nscd.service
           +-16470 /usr/sbin/nscd


[centos@ip-10-0-0-60 ~]$ sudo systemctl status nscd
? nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-10-17 08:24:28 UTC; 7h ago
 Main PID: 9396 (nscd)
   CGroup: /system.slice/nscd.service
           +-9396 /usr/sbin/nscd


[centos@ip-10-0-0-54 ~]$ getent hosts `hostname`
10.0.0.54       ip-10-0-0-54.eu-west-1.compute.internal
[centos@ip-10-0-0-54 ~]$ sudo systemctl status nscd
? nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-10-17 08:24:28 UTC; 7h ago
 Main PID: 9393 (nscd)
   CGroup: /system.slice/nscd.service
           +-9393 /usr/sbin/nscd


[centos@ip-10-0-0-16 ~]$ sudo systemctl status nscd
? nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-10-17 08:24:28 UTC; 7h ago
 Main PID: 9393 (nscd)
   CGroup: /system.slice/nscd.service
           +-9393 /usr/sbin/nscd


[centos@ip-10-0-0-250 ~]$ getent hosts `hostname`
10.0.0.250      ip-10-0-0-250.eu-west-1.compute.internal
[centos@ip-10-0-0-250 ~]$ sudo systemctl status nscd
? nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-10-17 08:24:28 UTC; 7h ago
 Main PID: 9512 (nscd)
   CGroup: /system.slice/nscd.service
           +-9512 /usr/sbin/nscd




###ntpd service is running
sudo yum install ntp -y

[centos@ip-10-0-0-207 ~]$ sudo systemctl status ntpd
? ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-10-17 08:25:26 UTC; 7h ago
 Main PID: 16539 (ntpd)
   CGroup: /system.slice/ntpd.service
           +-16539 /usr/sbin/ntpd -u ntp:ntp -g

[centos@ip-10-0-0-60 ~]$ sudo systemctl status ntpd
? ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-10-17 08:25:26 UTC; 7h ago
 Main PID: 9465 (ntpd)
   CGroup: /system.slice/ntpd.service
           +-9465 /usr/sbin/ntpd -u ntp:ntp -g

[centos@ip-10-0-0-54 ~]$ sudo systemctl status ntpd
? ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-10-17 08:25:26 UTC; 7h ago
 Main PID: 9462 (ntpd)
   CGroup: /system.slice/ntpd.service
           +-9462 /usr/sbin/ntpd -u ntp:ntp -g

[centos@ip-10-0-0-16 ~]$ sudo systemctl status ntpd
? ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-10-17 08:25:26 UTC; 7h ago
 Main PID: 9462 (ntpd)
   CGroup: /system.slice/ntpd.service
           +-9462 /usr/sbin/ntpd -u ntp:ntp -g


[centos@ip-10-0-0-250 ~]$ sudo systemctl status ntpd
? ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; disabled; vendor preset: disabled)
   Active: active (running) since Tue 2017-10-17 08:25:26 UTC; 7h ago
 Main PID: 9581 (ntpd)
   CGroup: /system.slice/ntpd.service
           +-9581 /usr/sbin/ntpd -u ntp:ntp -g





