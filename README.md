# Zabbix agent
Zabbix Agent, The Enterprise-Class Open Source Network Monitoring Agent.


Example(s)
----------------
```
- hosts: zabbix_agents
  become: true

  vars:

  roles:
    - role-zabbix-agent

  tasks:
```
# Troubleshooting

When trouble with installing after upgrading Ubuntu, clean up the old repositories.
```
rm /etc/apt/sources.list.d/zabbix-*
rm /etc/apt/trusted.gpg.d/zabbix-*
rm /var/lib/apt/lists/*zabbix*
rm /var/lib/dpkg/info/zabbix-release.*
rm /usr/share/doc/zabbix-release -r
rm /var/lib/systemd/deb-systemd-helper-masked/zabbix-agent.service
```

# Source(s)
- https://www.zabbix.com/
