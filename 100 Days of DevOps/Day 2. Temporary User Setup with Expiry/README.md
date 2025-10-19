# Day 2: Temporary User Setup with Expiry
As part of the temporary assignment to the `Nautilus` project, a developer named `james` requires access for a limited duration. To ensure smooth access management, a temporary user account with an expiry date is needed. Here's what you need to do:

Create a user named `james` on `App Server 3` in Stratos Datacenter. Set the expiry date to `2024-03-28`, ensuring the user is created in lowercase as per standard protocol.
> Note: You can find the infrastructure details by clicking on the Details of all Users and Servers button on the top-right section of the page.

## 1. Create a user named james on App Server 3
`sudo useradd james`

`cat /etc/shadow`
```console
james:!!:20380:0:99999:7:::
```

## 2. Set the expiry date to `2024-03-28`
`sudo usermod -e 2024-03-28 james`

`cat /etc/shadow`           
```console
james:!!:20380:0:99999:7::19810:
```