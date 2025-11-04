# Day 5. SElinux Installation and Configuration

## 1. Install the required `SELinux` packages.
`sudo yum update`
`sudo yum install selinux-policy selinux-policy-targeted policycoreutils`

`rpm -aq | grep selinux`

`sestatus`
```console
SELinux status:                 disabled
```

## 2. Disable `SELinux`.
`cat /etc/selinux/config | grep SELINUX=`
```console
# SELINUX= can take one of these three values:
# NOTE: Up to RHEL 8 release included, SELINUX=disabled would also
SELINUX=disabled
```