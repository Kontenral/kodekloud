# Secure Data Transfer
A `Nautilus` developer has stored confidential data on the jump host within `Stratos DC`. To ensure security and compliance, this data must be transferred to one of the app servers. Given developers lack direct access to these servers, the system admin team has been enlisted for assistance.

Copy `/tmp/nautilus.txt.gpg` file from jump server to App Server 1 placing it in the directory `/home/web`.

## 1. Copy `/tmp/nautilus.txt.gpg` file from jump server to App Server 1 placing it in the directory `/home/web`
`scp /tmp/nautilus.txt.gpg tony@stapp01:/home/web`
