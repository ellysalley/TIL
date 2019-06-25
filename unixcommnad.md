## Unix / linux file related 
--

# No space left on device – running out of Inodes

```
$ df 
$ df -i
```

on root directory
```
$ sudo du -x / | sort -n | tail -40
```

In this case, there are so many linux header files

```
$ apt-get autoremove
```

But our file system already full, so delete some files manually, and try again.

```
Filesystem     Inodes  IUsed  IFree IUse% Mounted on
udev           124458    360 124098    1% /dev
tmpfs          126779    475 126304    1% /run
/dev/xvda1     524288 425799  98489   82% /
tmpfs          126779      1 126778    1% /dev/shm
tmpfs          126779      5 126774    1% /run/lock
tmpfs          126779     16 126763    1% /sys/fs/cgroup
tmpfs          126779      4 126775    1% /run/user/1000
```