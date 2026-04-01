# Automated Zabbix Monitoring using Ansible

## 📌 Overview
This project automates the complete onboarding of Linux servers into Zabbix monitoring using Ansible.

It performs:
- Zabbix agent installation
- Agent configuration (active + passive checks)
- Host registration via Zabbix API
- Template linking for monitoring

---

## 🧠 Architecture

Control Flow:

Ansible Control Node
│
├── SSH → Target Servers (Install + Configure Agent)
└── HTTP API → Zabbix Server (Register Hosts)

---

## ⚙️ Tech Stack

- Ansible
- Zabbix 7.x
- Linux (Ubuntu + Amazon Linux)
- REST API (Zabbix JSON-RPC)

---

## 📂 Project Structure



---

## 🚀 How It Works

### Step 1: Inventory
Define servers in:

inventory.ini

---

### Step 2: Agent Setup
Ansible installs and configures Zabbix agent on all hosts.

---

### Step 3: API Registration
Hosts are registered in Zabbix via API using Ansible httpapi plugin.

---

### Step 4: Monitoring Starts
Zabbix begins collecting metrics from agents.

---

## ▶️ Run the Playbook

```bash
ansible-playbook -i inventory.ini playbook.yml

```

---
## ⚠️ Notes
AWS instances used for testing were temporary and may not be available anymore
Replace IPs and credentials before running
---

