# String Replacement
Within the Stratos DC, the backup server holds template XML files crucial for the Nautilus application. Before utilization, these files require valid data insertion. As part of routine maintenance, system admins at `xFusionCorp Industries` employ string and file manipulation commands.

Your task is to substitute all occurrences of the string `Random` with `Maritime` within the XML file located at `/root/nautilus.xml` on the backup server.

## 1. Substitute all occurrences of the string `Random` with `Maritime` within the XML file located at `/root/nautilus.xml`
`sudo sed -i 's/Random/Maritime/g' /root/nautilus.xml`
