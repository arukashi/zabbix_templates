`/etc/zabbix/zabbix_agentd.conf.d/userparameter_ipmitool.conf  `
```
UserParameter=ipmitool.sensors.status,/usr/bin/sudo ipmitool sdr
```

`/etc/sudoers.d/sudoers_zabbix_ipmitool`
```
Cmnd_Alias IPMITOOL = /usr/bin/ipmitool
zabbix ALL= (ALL) NOPASSWD: IPMITOOL
Defaults!IPMITOOL !logfile, !syslog, !pam_session
```
