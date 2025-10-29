# Service User Creation without Home Directory
In response to the latest tool implementation at `xFusionCorp Industries`, the system admins require the creation of a service user account. Here are the specifics:

Create a user named `rose` in `App Server 2` without a home directory.

> Note: You can find the infrastructure details by clicking on the Details of all Users and Servers button on the top-right section of the page.

## 1. Create a user named `rose` in `App Server 2` without a home directory
`cat /etc/passwd | grep rose`

`sudo useradd -M rose`
