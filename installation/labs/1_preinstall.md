########CM Install Lab#######

###swappiness###
[root@ip-10-0-0-253 centos]# sysctl vm.swappiness=1
vm.swappiness = 1
[root@ip-10-0-0-253 centos]# cat /proc/sys/vm/swappiness
1

[root@ip-10-0-0-158 centos]# sysctl vm.swappiness=1
vm.swappiness = 1
[root@ip-10-0-0-158 centos]# cat /proc/sys/vm/swappiness
1
[root@ip-10-0-0-158 centos]#


[root@ip-10-0-0-79 centos]# sysctl vm.swappiness=1
vm.swappiness = 1
[root@ip-10-0-0-79 centos]# cat /proc/sys/vm/swappiness
1
[root@ip-10-0-0-79 centos]#


[root@ip-10-0-0-250 centos]# sysctl vm.swappiness=1
vm.swappiness = 1
[root@ip-10-0-0-250 centos]# cat /proc/sys/vm/swappiness
1
[root@ip-10-0-0-250 centos]#


[root@ip-10-0-0-94 centos]# sysctl vm.swappiness=1
vm.swappiness = 1
[root@ip-10-0-0-94 centos]# cat /proc/sys/vm/swappiness
1
[root@ip-10-0-0-94 centos]#


###mount###
[root@ip-10-0-0-253 centos]# mount
/dev/xvda1 on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
/dev/xvdb on /mnt type ext3 (rw,_netdev)


[root@ip-10-0-0-158 centos]# mount
/dev/xvda1 on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
/dev/xvdb on /mnt type ext3 (rw,_netdev)


[root@ip-10-0-0-79 centos]# mount
/dev/xvda1 on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
/dev/xvdb on /mnt type ext3 (rw,_netdev)


[root@ip-10-0-0-250 centos]# mount
/dev/xvda1 on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
/dev/xvdb on /mnt type ext3 (rw,_netdev)


[root@ip-10-0-0-94 centos]# mount
/dev/xvda1 on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
/dev/xvdb on /mnt type ext3 (rw,_netdev)




###reserve space
[root@ip-10-0-0-253 centos]# df -hT
Filesystem     Type   Size  Used Avail Use% Mounted on
/dev/xvda1     ext4   7.8G  666M  6.7G   9% /
tmpfs          tmpfs  7.3G     0  7.3G   0% /dev/shm
/dev/xvdb      ext3    37G  177M   35G   1% /mnt

[root@ip-10-0-0-158 centos]# df -hT
Filesystem     Type   Size  Used Avail Use% Mounted on
/dev/xvda1     ext4   7.8G  666M  6.7G   9% /
tmpfs          tmpfs  7.3G     0  7.3G   0% /dev/shm
/dev/xvdb      ext3    37G  177M   35G   1% /mnt

[root@ip-10-0-0-79 centos]# df -hT
Filesystem     Type   Size  Used Avail Use% Mounted on
/dev/xvda1     ext4   7.8G  666M  6.7G   9% /
tmpfs          tmpfs  7.3G     0  7.3G   0% /dev/shm
/dev/xvdb      ext3    37G  177M   35G   1% /mnt

[root@ip-10-0-0-250 centos]# df -hT
Filesystem     Type   Size  Used Avail Use% Mounted on
/dev/xvda1     ext4   7.8G  666M  6.7G   9% /
tmpfs          tmpfs  7.3G     0  7.3G   0% /dev/shm
/dev/xvdb      ext3    37G  177M   35G   1% /mnt

[root@ip-10-0-0-94 centos]# df -hT
Filesystem     Type   Size  Used Avail Use% Mounted on
/dev/xvda1     ext4   7.8G  666M  6.7G   9% /
tmpfs          tmpfs  7.3G     0  7.3G   0% /dev/shm
/dev/xvdb      ext3    37G  177M   35G   1% /mnt



###Disable transparent hugepage support
[root@ip-10-0-0-253 centos]# cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never

[root@ip-10-0-0-158 centos]# cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never


[root@ip-10-0-0-79 centos]# cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never


[root@ip-10-0-0-250 centos]# cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never

[root@ip-10-0-0-94 centos]# cat /sys/kernel/mm/transparent_hugepage/enabled
[always] madvise never



###Network interface configuaration
[root@ip-10-0-0-253 centos]# ifconfig
eth0      Link encap:Ethernet  HWaddr 0A:B9:76:AD:EA:16
          inet addr:10.0.0.253  Bcast:10.0.0.255  Mask:255.255.255.0
          inet6 addr: fe80::8b9:76ff:fead:ea16/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:525 errors:0 dropped:0 overruns:0 frame:0
          TX packets:462 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:52333 (51.1 KiB)  TX bytes:57156 (55.8 KiB)
          Interrupt:143

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

		  
[root@ip-10-0-0-158 centos]# ifconfig
eth0      Link encap:Ethernet  HWaddr 0A:96:C0:02:46:62
          inet addr:10.0.0.158  Bcast:10.0.0.255  Mask:255.255.255.0
          inet6 addr: fe80::896:c0ff:fe02:4662/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:557 errors:0 dropped:0 overruns:0 frame:0
          TX packets:552 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:57802 (56.4 KiB)  TX bytes:68851 (67.2 KiB)
          Interrupt:143

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

[root@ip-10-0-0-79 centos]# ifconfig
eth0      Link encap:Ethernet  HWaddr 0A:59:AA:3A:61:56
          inet addr:10.0.0.79  Bcast:10.0.0.255  Mask:255.255.255.0
          inet6 addr: fe80::859:aaff:fe3a:6156/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:487 errors:0 dropped:0 overruns:0 frame:0
          TX packets:501 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:51086 (49.8 KiB)  TX bytes:58815 (57.4 KiB)
          Interrupt:143

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

[root@ip-10-0-0-250 centos]# ifconfig
eth0      Link encap:Ethernet  HWaddr 0A:1D:A2:BF:9B:80
          inet addr:10.0.0.250  Bcast:10.0.0.255  Mask:255.255.255.0
          inet6 addr: fe80::81d:a2ff:febf:9b80/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:491 errors:0 dropped:0 overruns:0 frame:0
          TX packets:491 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:50534 (49.3 KiB)  TX bytes:56514 (55.1 KiB)
          Interrupt:143

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

[root@ip-10-0-0-94 centos]# ifconfig
eth0      Link encap:Ethernet  HWaddr 0A:51:C0:0E:A3:5A
          inet addr:10.0.0.94  Bcast:10.0.0.255  Mask:255.255.255.0
          inet6 addr: fe80::851:c0ff:fe0e:a35a/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:532 errors:0 dropped:0 overruns:0 frame:0
          TX packets:537 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:59344 (57.9 KiB)  TX bytes:67818 (66.2 KiB)
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
[root@ip-10-0-0-253 centos]# getent hosts `hostname`
10.0.0.253      ip-10-0-0-253.eu-west-1.compute.internal

[root@ip-10-0-0-158 centos]# getent hosts `hostname`
10.0.0.158      ip-10-0-0-158.eu-west-1.compute.internal

[root@ip-10-0-0-79 centos]# getent hosts `hostname`
10.0.0.79       ip-10-0-0-79.eu-west-1.compute.internal

[root@ip-10-0-0-250 centos]# getent hosts `hostname`
10.0.0.250      ip-10-0-0-250.eu-west-1.compute.internal

[root@ip-10-0-0-94 centos]# getent hosts `hostname`
10.0.0.94       ip-10-0-0-94.eu-west-1.compute.internal





###nscd service is running
yum install nscd -y

[root@ip-10-0-0-253 centos]# /etc/init.d/nscd start
Starting nscd:                                             [  OK  ]
[root@ip-10-0-0-253 centos]# /etc/init.d/nscd status
nscd (pid 1670) is running...

[root@ip-10-0-0-158 centos]# /etc/init.d/nscd start
Starting nscd:                                             [  OK  ]
[root@ip-10-0-0-158 centos]# /etc/init.d/nscd status
nscd (pid 5108) is running...

[root@ip-10-0-0-79 centos]# /etc/init.d/nscd start
Starting nscd:                                             [  OK  ]
[root@ip-10-0-0-79 centos]# /etc/init.d/nscd status
nscd (pid 5123) is running...

[root@ip-10-0-0-250 centos]# /etc/init.d/nscd start
Starting nscd:                                             [  OK  ]
[root@ip-10-0-0-250 centos]# /etc/init.d/nscd status
nscd (pid 1669) is running...

[root@ip-10-0-0-94 centos]# /etc/init.d/nscd start
Starting nscd:                                             [  OK  ]
[root@ip-10-0-0-94 centos]# /etc/init.d/nscd status
nscd (pid 5128) is running...



###ntpd service is running
yum install ntp -y
[root@ip-10-0-0-253 centos]# /etc/init.d/ntpd start
Starting ntpd:                                             [  OK  ]
[root@ip-10-0-0-253 centos]# /etc/init.d/ntpd status
ntpd (pid  1749) is running...

[root@ip-10-0-0-158 centos]# /etc/init.d/ntpd start
Starting ntpd:                                             [  OK  ]
[root@ip-10-0-0-158 centos]# /etc/init.d/ntpd status
ntpd (pid  5186) is running...

[root@ip-10-0-0-79 centos]# /etc/init.d/ntpd start
Starting ntpd:                                             [  OK  ]
[root@ip-10-0-0-79 centos]# /etc/init.d/ntpd status
ntpd (pid  5197) is running...

[root@ip-10-0-0-250 centos]# /etc/init.d/ntpd start
Starting ntpd:                                             [  OK  ]
[root@ip-10-0-0-250 centos]# /etc/init.d/ntpd status
ntpd (pid  1765) is running...

[root@ip-10-0-0-94 centos]# /etc/init.d/ntpd start
Starting ntpd:                                             [  OK  ]
[root@ip-10-0-0-94 centos]# /etc/init.d/ntpd status
ntpd (pid  5202) is running...




