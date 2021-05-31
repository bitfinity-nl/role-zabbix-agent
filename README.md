# role-zabbix-agent
Zabbix Agent, The Enterprise-Class Open Source Network Monitoring Agent.


Example(s)
----------------

# Zabbix Agent (Ubuntu 20.04lts AMD64)
```
- hosts: zabbix-server
  become: yes

  vars:
    # -- roles/role-zabbix-5 --
    zbx_type : 'server'  # Set zabbix type to "server".

  roles:
    - role-zabbix-agent

  tasks:
```
