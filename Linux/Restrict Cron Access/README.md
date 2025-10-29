# Restrict Cron Access
In alignment with security compliance standards, the Nautilus project team has opted to impose restrictions on crontab access. Specifically, only designated users will be permitted to create or update cron jobs.

Configure crontab access on App Server 3 as follows: Allow crontab access to `james` user while denying access to the `eric` user.

## 1. Configure crontab access on App Server 3 as follows: Allow crontab access to `james` user while denying access to the `eric` user.
`echo "james" | sudo tee /etc/cron.allow`

`echo "eric" | sudo tee -a /etc/cron.deny`

`sudo chmod 600 /etc/cron.allow`
`sudo chown root:root /etc/cron.allow`