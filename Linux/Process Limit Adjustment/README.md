# Process Limit Adjustment
In the `Stratos Datacenter`, our `Storage server` is encountering performance degradation due to excessive processes held by the `nfsuser` user. To mitigate this issue, we need to enforce limitations on its maximum processes. Please set the maximum process limits as specified below:

a. Set the soft limit to `1026`

b. Set the hard limit to `2026`

## 1. Set the soft limit to `1026` and set the hard limit to `2026`
`sudo vi /etc/security/limits.conf`

`sudo cat /etc/security/limits.conf | grep nfsuser`
```console
nfsuser         soft    nproc   1026
nfsuser         hard    nproc   2026
```

## 2. Check if settings applied
`sudo su - nfsuser -c "ulimit -u"`

`sudo su - nfsuser`
`ulimit -Su   # soft limit`
`ulimit -Hu   # hard limit`