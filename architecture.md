
---

# 6) architecture.md (Optional but Strong)

```markdown
# Architecture

## Components

1. Ansible Control Node
2. Target Linux Servers
3. Zabbix Server

## Flow

1. Ansible connects via SSH → installs agent
2. Agent configured to talk to Zabbix server
3. Ansible calls Zabbix API → creates host
4. Zabbix links template → starts monitoring
