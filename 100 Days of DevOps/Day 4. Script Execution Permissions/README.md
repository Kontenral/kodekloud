# Day 4: Script Execution Permissions
In a bid to automate backup processes, the `xFusionCorp Industries` sysadmin team has developed a new bash script named `xfusioncorp.sh`. While the script has been distributed to all necessary servers, it lacks executable permissions on `App Server 2` within the Stratos Datacenter.

Your task is to grant executable permissions to the `/tmp/xfusioncorp.sh` script on `App Server 2`. Additionally, ensure that all users have the capability to execute it.

## 1. Grant executable permissions to the `/tmp/xfusioncorp.sh` script
`ls -la /tmp/xfusioncorp.sh`
```console
---------- 1 root root 40 Oct 20 14:39 /tmp/xfusioncorp.sh
```

`sudo chmod 755 /tmp/xfusioncorp.sh`
`ls -la /tmp/xfusioncorp.sh`
```console
-rwxr-xr-x 1 root root 40 Oct 20 14:39 /tmp/xfusioncorp.sh
```
