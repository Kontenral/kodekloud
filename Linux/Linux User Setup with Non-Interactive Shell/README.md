# Linux User Setup with Non-Interactive Shell
To accommodate the backup agent tool's specifications, the system admin team at `xFusionCorp Industries` requires the creation of a user with a non-interactive shell. Here's your task:

Create a user named `mark` with a non-interactive shell on `App Server 2`.
> Note: You can find the infrastructure details by clicking on the **Details of all Users and Servers** button on the top-right section of the page.

## 1. Create a user named `mark` with a non-interactive shell
`sudo useradd -s /sbin/nologin mark`

`sudo cat /etc/passwd | grep mark`
```console
mark:x:1002:1002::/home/mark:/sbin/nologin
```