# role-zabbix-agent
Zabbix Agent, The Enterprise-Class Open Source Network Monitoring Agent.


Example(s)
----------------

# Zabbix Agent (Ubuntu 20.04lts AMD64)
```
- hosts: zabbix-server
  become: yes

  vars:
    # -- roles/role-zabbix-agent --
    zbx_agt_HostMetadata : 'Server'

  roles:
    - role-zabbix-agent

  tasks:
```
