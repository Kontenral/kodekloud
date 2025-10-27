# Secure ssh root access
Following security audits, the `xFusionCorp Industries` security team has rolled out new protocols, including the restriction of direct root SSH login.

Your task is to disable direct SSH root login on all app servers within the `Stratos Datacenter`.

## 1. Disable direct SSH root login on all app servers within the `Stratos Datacenter`
`sudo -s`
`echo "PermitRootLogin no" >> /etc/ssh/sshd_config`
`sed -i 's/PermitRootLogin yes/PermitRootLogin no/g' /etc/ssh/sshd_config`

`cat /etc/ssh/sshd_config | grep -i root`
```console
PermitRootLogin yes
# the setting of "PermitRootLogin without-password".
#ChrootDirectory none
```

`systemctl restart sshd`