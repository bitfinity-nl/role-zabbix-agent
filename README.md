# role-zabbix-agent
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
