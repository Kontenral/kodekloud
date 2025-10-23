# Custom Apache User Setup

In response to heightened security concerns, the `xFusionCorp Industries` security team has opted for custom Apache users for their web applications. Each user is tailored specifically for an application, enhancing security measures. Your task is to create a custom Apache user according to the outlined specifications:

a. Create a user named `javed` on `App server 2` within the Stratos Datacenter.

b. Assign a unique UID `1086` and designate the home directory as `/var/www/javed`.
> Note: You can find the infrastructure details by clicking on the Details of all Users and Servers button on the top-right section of the page.

## 1. Create a user named `javed` on `App server 2`
`sudo useradd javed`

`sudo cat /etc/passwd | grep javed`
```console
javed:x:1002:1002::/home/javed:/bin/bash
```

## 2. Assign a unique UID `1086` and designate the home directory as `/var/www/javed`
`usermod -m -d /var/www/javed -u 1086`

`sudo cat /etc/passwd | grep javed`
```console
javed:x:1086:1002::/var/www/javed:/bin/bash
```

