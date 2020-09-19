# fail2ban-zimbra

jail.conf

```
[zimbra-submission]
enabled = true
filter = zimbra-submission
logpath = /var/log/zimbra.log
maxretry = 3
findtime = 3600
bantime = 7200
action = iptables-multiport[name=zimbra-submission, port="25,465,587", protocol=tcp]

[zimbra-web]
enabled = true
filter = zimbra-web
logpath = /opt/zimbra/log/mailbox.log
maxretry = 3
findtime = 3600
bantime = 7200
action = iptables-multiport[name=zimbra-web, port="80,443,7071", protocol=tcp]
```
