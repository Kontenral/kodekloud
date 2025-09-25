# Set Up Git Repository on Storage Server

The Nautilus development team has provided requirements to the DevOps team for a new application development project, specifically requesting the establishment of a Git repository. Follow the instructions below to create the Git repository on the `Storage server` in the Stratos DC:

Utilize yum to install the git package on the `Storage Server`.

Create a bare repository named `/opt/games.git` (ensure exact name usage).

## 1. Install Git on Storage Server

`ssh natasha@ststor01`

`sudo -s`

`hostnamectl`

```console
 Static hostname: ststor01.stratos.xfusioncorp.com
       Icon name: computer-container
         Chassis: container ☐
      Machine ID: ce131cf36c8149f9a5285064fd7c61a0
         Boot ID: 65dc3786ac2c47909622a5ecd15eb622
  Virtualization: docker
Operating System: CentOS Stream 9                 
     CPE OS Name: cpe:/o:centos:centos:9
          Kernel: Linux 5.4.0-1106-gcp
    Architecture: x86-64
Firmware Version: Google
```

## 2. Setup user Git config


## 3. Create a bare repository