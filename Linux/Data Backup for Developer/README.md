# Data Backup for Developer
Within the Stratos DC, the Nautilus storage server hosts a directory named `/data`, serving as a repository for various developers non-confidential data. Developer `siva` has requested a copy of their data stored in `/data/siva`. The System Admin team has provided the following steps to fulfill this request:

a. Create a compressed archive named `siva.tar.gz` of the `/data/siva` directory.

b. Transfer the archive to the `/home` directory on the Storage Server.

## 1. Create a compressed archive named `siva.tar.gz` of the `/data/siva` directory.
`tar cvfz siva.tar.gz /data/siva/`

## 2. Transfer the archive to the `/home` directory on the Storage Server
`mv siva.tar.gz /home/`