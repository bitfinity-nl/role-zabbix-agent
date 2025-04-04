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
#!/bin/bash
clear

echo "... Clear Zabbix legacy links"
rm /etc/apt/sources.list.d/zabbix*
rm /etc/apt/trusted.gpg.d/zabbix*
rm /var/lib/apt/lists/*zabbix*
rm /var/lib/dpkg/info/zabbix-release.*
rm /usr/share/doc/zabbix-release -r
rm /var/lib/systemd/deb-systemd-helper-masked/zabbix-agent.service
echo ""

echo "... Check if zabbix files are removed from directory /etc/apt/sources.list.d/"
ls -al /etc/apt/sources.list.d/
echo "... Check if zabbix files are removed from directory /etc/apt/trusted.gpg.d/"
ls -al /etc/apt/trusted.gpg.d/
echo ""

echo "... Install zabbix repository"
dpkg -i zabbix-release_latest_7.0+ubuntu24.04_all.deb
echo ""

echo "... Check if zabbix files are removed from directory /etc/apt/sources.list.d/"
ls -al /etc/apt/sources.list.d/
echo "... Check if zabbix files are removed from directory /etc/apt/trusted.gpg.d/"
ls -al /etc/apt/trusted.gpg.d/
echo ""
```

# Source(s)
- https://www.zabbix.com/
