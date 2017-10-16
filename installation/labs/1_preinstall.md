########CM Install Lab#######

###swappiness###
[centos@ip-10-0-0-141 ~]$ sudo sysctl vm.swappiness=1
vm.swappiness = 1
[centos@ip-10-0-0-141 ~]$ cat /proc/sys/vm/swappiness
1

[centos@ip-10-0-0-74 ~]$ sudo sysctl vm.swappiness=1
vm.swappiness = 1
[centos@ip-10-0-0-74 ~]$ cat /proc/sys/vm/swappiness
1

[centos@ip-10-0-0-211 ~]$ sudo sysctl vm.swappiness=1
vm.swappiness = 1
[centos@ip-10-0-0-211 ~]$ cat /proc/sys/vm/swappiness
1

[centos@ip-10-0-0-249 ~]$ sudo sysctl vm.swappiness=1
vm.swappiness = 1
[centos@ip-10-0-0-249 ~]$ cat /proc/sys/vm/swappiness
1

[centos@ip-10-0-0-134 ~]$ sudo sysctl vm.swappiness=1
vm.swappiness = 1
[centos@ip-10-0-0-134 ~]$ cat /proc/sys/vm/swappiness
1



###mount###
[centos@ip-10-0-0-141 ~]$ mount
/dev/xvda1 on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
/dev/xvdb on /mnt type ext3 (rw,_netdev)

[centos@ip-10-0-0-74 ~]$ mount
/dev/xvda1 on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
/dev/xvdb on /mnt type ext3 (rw,_netdev)

[centos@ip-10-0-0-211 ~]$ mount
/dev/xvda1 on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
/dev/xvdb on /mnt type ext3 (rw,_netdev)

[centos@ip-10-0-0-249 ~]$ mount
/dev/xvda1 on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
/dev/xvdb on /mnt type ext3 (rw,_netdev)

[centos@ip-10-0-0-134 ~]$ mount
/dev/xvda1 on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
/dev/xvdb on /mnt type ext3 (rw,_netdev)



###reserve space
[centos@ip-10-0-0-141 ~]$ df -hT
Filesystem     Type   Size  Used Avail Use% Mounted on
/dev/xvda1     ext4   7.8G  666M  6.7G   9% /
tmpfs          tmpfs  7.3G     0  7.3G   0% /dev/shm
/dev/xvdb      ext3    37G  177M   35G   1% /mnt

[centos@ip-10-0-0-74 ~]$ df -hT
Filesystem     Type   Size  Used Avail Use% Mounted on
/dev/xvda1     ext4   7.8G  666M  6.7G   9% /
tmpfs          tmpfs  7.3G     0  7.3G   0% /dev/shm
/dev/xvdb      ext3    37G  177M   35G   1% /mnt

[centos@ip-10-0-0-211 ~]$ df -hT
Filesystem     Type   Size  Used Avail Use% Mounted on
/dev/xvda1     ext4   7.8G  666M  6.7G   9% /
tmpfs          tmpfs  7.3G     0  7.3G   0% /dev/shm
/dev/xvdb      ext3    37G  177M   35G   1% /mnt

[centos@ip-10-0-0-249 ~]$ df -hT
Filesystem     Type   Size  Used Avail Use% Mounted on
/dev/xvda1     ext4   7.8G  666M  6.7G   9% /
tmpfs          tmpfs  7.3G     0  7.3G   0% /dev/shm
/dev/xvdb      ext3    37G  177M   35G   1% /mnt

[centos@ip-10-0-0-134 ~]$ df -hT
Filesystem     Type   Size  Used Avail Use% Mounted on
/dev/xvda1     ext4   7.8G  666M  6.7G   9% /
tmpfs          tmpfs  7.3G     0  7.3G   0% /dev/shm
/dev/xvdb      ext3    37G  177M   35G   1% /mnt



###Disable transparent hugepage support
[centos@ip-10-0-0-141 ~]$ cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never

[centos@ip-10-0-0-74 ~]$ cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never

[centos@ip-10-0-0-211 ~]$ cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never

[centos@ip-10-0-0-249 ~]$ cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never

[centos@ip-10-0-0-134 ~]$ cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never


###Network interface configuaration
[centos@ip-10-0-0-141 ~]$  ifconfig
eth0      Link encap:Ethernet  HWaddr 0A:CB:09:F0:BD:16
          inet addr:10.0.0.141  Bcast:10.0.0.255  Mask:255.255.255.0
          inet6 addr: fe80::8cb:9ff:fef0:bd16/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:582 errors:0 dropped:0 overruns:0 frame:0
          TX packets:511 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:54666 (53.3 KiB)  TX bytes:59842 (58.4 KiB)
          Interrupt:143

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

eth0      Link encap:Ethernet  HWaddr 0A:65:9B:A5:07:DE
          inet addr:10.0.0.74  Bcast:10.0.0.255  Mask:255.255.255.0
          inet6 addr: fe80::865:9bff:fea5:7de/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:575 errors:0 dropped:0 overruns:0 frame:0
          TX packets:490 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:55000 (53.7 KiB)  TX bytes:59757 (58.3 KiB)
          Interrupt:143

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

eth0      Link encap:Ethernet  HWaddr 0A:72:AC:94:EE:E6
          inet addr:10.0.0.211  Bcast:10.0.0.255  Mask:255.255.255.0
          inet6 addr: fe80::872:acff:fe94:eee6/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:513 errors:0 dropped:0 overruns:0 frame:0
          TX packets:469 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:49925 (48.7 KiB)  TX bytes:54517 (53.2 KiB)
          Interrupt:143

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

eth0      Link encap:Ethernet  HWaddr 0A:CF:7C:F4:01:C2
          inet addr:10.0.0.249  Bcast:10.0.0.255  Mask:255.255.255.0
          inet6 addr: fe80::8cf:7cff:fef4:1c2/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:511 errors:0 dropped:0 overruns:0 frame:0
          TX packets:471 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:49848 (48.6 KiB)  TX bytes:54553 (53.2 KiB)
          Interrupt:143

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

eth0      Link encap:Ethernet  HWaddr 0A:BE:7E:28:FE:66
          inet addr:10.0.0.134  Bcast:10.0.0.255  Mask:255.255.255.0
          inet6 addr: fe80::8be:7eff:fe28:fe66/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:517 errors:0 dropped:0 overruns:0 frame:0
          TX packets:472 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:50044 (48.8 KiB)  TX bytes:54479 (53.2 KiB)
          Interrupt:143

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)
 
		  
###forward and reverse host lookups
[centos@ip-10-0-0-141 ~]$ getent hosts `hostname`
10.0.0.141      ip-10-0-0-141.eu-west-1.compute.internal

[centos@ip-10-0-0-74 ~]$ getent hosts `hostname`
10.0.0.74       ip-10-0-0-74.eu-west-1.compute.internal

[centos@ip-10-0-0-211 ~]$ getent hosts `hostname`
10.0.0.211      ip-10-0-0-211.eu-west-1.compute.internal

[centos@ip-10-0-0-249 ~]$ getent hosts `hostname`
10.0.0.249      ip-10-0-0-249.eu-west-1.compute.internal

[centos@ip-10-0-0-134 ~]$ getent hosts `hostname`
10.0.0.134      ip-10-0-0-134.eu-west-1.compute.internal



###nscd service is running
sudo yum install nscd -y

[centos@ip-10-0-0-141 ~]$ sudo /etc/init.d/nscd start
Starting nscd:                                             [  OK  ]
[centos@ip-10-0-0-141 ~]$ sudo /etc/init.d/nscd status
nscd (pid 1580) is running...

[centos@ip-10-0-0-74 ~]$ sudo /etc/init.d/nscd start
Starting nscd:                                             [  OK  ]
[centos@ip-10-0-0-74 ~]$ sudo /etc/init.d/nscd status
nscd (pid 1586) is running...

[centos@ip-10-0-0-211 ~]$ sudo /etc/init.d/nscd start
Starting nscd:                                             [  OK  ]
[centos@ip-10-0-0-211 ~]$ sudo /etc/init.d/nscd status
nscd (pid 1581) is running...

[centos@ip-10-0-0-249 ~]$ sudo /etc/init.d/nscd start
Starting nscd:                                             [  OK  ]
[centos@ip-10-0-0-249 ~]$ sudo /etc/init.d/nscd status
nscd (pid 1575) is running...

[centos@ip-10-0-0-134 ~]$ sudo /etc/init.d/nscd start
Starting nscd:                                             [  OK  ]
[centos@ip-10-0-0-134 ~]$ sudo /etc/init.d/nscd status
nscd (pid 1581) is running...


###ntpd service is running
sudo yum install ntp -y

[centos@ip-10-0-0-141 ~]$ sudo /etc/init.d/ntpd start
Starting ntpd:                                             [  OK  ]
[centos@ip-10-0-0-141 ~]$ sudo /etc/init.d/ntpd status
ntpd (pid  1628) is running...

[centos@ip-10-0-0-74 ~]$ sudo /etc/init.d/ntpd start
Starting ntpd:                                             [  OK  ]
[centos@ip-10-0-0-74 ~]$ sudo /etc/init.d/ntpd status
ntpd (pid  1634) is running...

[centos@ip-10-0-0-211 ~]$ sudo /etc/init.d/ntpd start
Starting ntpd:                                             [  OK  ]
[centos@ip-10-0-0-211 ~]$ sudo /etc/init.d/ntpd status
ntpd (pid  1629) is running...

[centos@ip-10-0-0-249 ~]$ sudo /etc/init.d/ntpd start
Starting ntpd:                                             [  OK  ]
[centos@ip-10-0-0-249 ~]$ sudo /etc/init.d/ntpd status
ntpd (pid  1623) is running...

[centos@ip-10-0-0-134 ~]$ sudo /etc/init.d/ntpd start
Starting ntpd:                                             [  OK  ]
[centos@ip-10-0-0-134 ~]$ sudo /etc/init.d/ntpd status
ntpd (pid  1629) is running...




