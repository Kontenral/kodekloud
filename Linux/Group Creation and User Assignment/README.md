# Group Creation and User Assignment
The system admin team at `xFusionCorp Industrie`s has streamlined access management by implementing group-based access control. Here's what you need to do:

a. Create a group named `nautilus_developers` across all `App servers` within the `Stratos Datacenter`.

b. Add the user `sonya` into the `nautilus_developers` group on all App servers. If the user doesn't exist, create it as well.

> Note: You can find the infrastructure details by clicking on the Details of all Users and Servers button on the top-right section of the page.

## 1. Create a group named `nautilus_developers` across all `App servers`
`sudo groupadd nautilus_developers`

`cut -d: -f1 /etc/group | grep nautilus_developers`
```console
nautilus_developers
```

## 2. Add the user `sonya` into the `nautilus_developers`
`sudo useradd -m sonya`

`sudo usermod -aG nautilus_developers sonya`

`cat /etc/group | grep nautilus_developers`
```console
nautilus_developers:x:1002:sonya
```