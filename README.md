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
    zbx_agt_HostMetadata : 'Server,Ubuntu'
    zbx_server           : '10.1.30.31'
    zbx_active_server    : '{{ def_zbx_active_server }}'

  roles:
    - role-zabbix-agent

  tasks:
```
