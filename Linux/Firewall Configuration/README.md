# Firewall Configuration
The Nautilus system admins team has rolled out a web UI application for their backup utility on the Nautilus backup server within the Stratos Datacenter. This application operates on port 6200, and firewalld is active on the server. To meet operational needs, the following requirements have been identified:

Allow all incoming connections on port 6200/tcp. Ensure the zone is set to public.

## 1. Allow all incoming connections on port 6200/tcp. Ensure the zone is set to public.
`sudo firewall-cmd --state`
`sudo firewall-cmd --get-active-zones`
`sudo firewall-cmd --zone=public --add-port=6200/tcp --permanent`
`sudo firewall-cmd --reload`
`sudo firewall-cmd --zone=public --list-ports`