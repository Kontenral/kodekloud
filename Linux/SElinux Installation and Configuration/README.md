# SElinux Installation and Configuration
Following a security audit, the xFusionCorp Industries security team has opted to enhance application and server security with SELinux. To initiate testing, the following requirements have been established for `App server 1` in the `Stratos Datacenter`:

Install the required `SELinux` packages.

Permanently disable SELinux for the time being; it will be re-enabled after necessary configuration changes.

No need to reboot the server, as a scheduled maintenance reboot is already planned for tonight.

Disregard the current status of SELinux via the command line; the final status after the reboot should be `disabled`.

## 1. Install the required `SELinux` packages.
`sudo yum install selinux-policy selinux-policy-targeted policycoreutils`

`rpm -aq | grep selinux`

`sestatus`
```console
SELinux status:                 disabled
```

`cat /etc/selinux/config | grep SELINUX=`
```console
# SELINUX= can take one of these three values:
# NOTE: Up to RHEL 8 release included, SELINUX=disabled would also
SELINUX=disabled
```