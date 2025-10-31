# Timezone Alignment
In the daily standup, it was noted that the timezone settings across the `Nautilus Application Servers` in the `Stratos Datacenter` are inconsistent with the local datacenter's timezone, currently set to `Asia/Khandyga`.

Synchronize the timezone settings to match the local datacenter's timezone (`Asia/Khandyga`).

## 1. Synchronize the timezone settings to match the local datacenter's timezone (`Asia/Khandyga`).
`sudo timedatectl set-timezone Asia/Khandyga`

`timedatectl`
```console
               Local time: Sat 2025-11-01 05:23:28 +09
           Universal time: Fri 2025-10-31 20:23:28 UTC
                 RTC time: n/a
                Time zone: Asia/Khandyga (+09, +0900)
System clock synchronized: yes
              NTP service: n/a
          RTC in local TZ: no
```