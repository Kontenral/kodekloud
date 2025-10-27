# Linux User Data Transfer
Locate all files (excluding directories) owned by user `kareem` within the `/home/usersdata `directory on `App Server 1`. Copy these files while preserving the directory structure to the /blog directory.

## 1. Locate all files (excluding directories) owned by user `kareem` within the `/home/usersdata `directory
`find /home/usersdata -type f -user kareem | wc -l`

`cd /home/usersdata`

`sudo find . -type f -user kareem -exec cp --parents -a -t /blog {} +`

`find /blog -type f -user kareem | wc -l`
