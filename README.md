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

AWS instances used for testing were temporary and may not be available anymore.
Replace IPs and credentials before running.


---


---

## 🔥 Key Learnings

- Infrastructure automation with Ansible
- API-driven system integration
- Multi-OS compatibility handling
- Idempotent configuration management
- Debugging real-world infra issues

---

---

## 📈 Future Improvements

Dynamic inventory (AWS EC2)
Zabbix auto-registration
Alerting & triggers automation
Role modularization
Secrets management using Ansible Vault

---

---

## Architecture Summary


                +----------------------+
                |  Ansible Control Node|
                |  (venv active)       |
                +----------+-----------+
                           |
        +------------------+------------------+
        |                                     |
   SSH (my-key.pem)                     HTTP API (httpapi)
        |                                     |
        v                                     v
+---------------+                   +----------------------+
| Target Server |                   |   Zabbix Server      |
| (Agent runs) |                   |  (API + UI)          |
+---------------+                   +----------------------+


---
## 📸 Screenshots

<img width="1473" height="650" alt="Screenshot 2026-04-02 at 3 37 47 AM" src="https://github.com/user-attachments/assets/6dcac78a-8283-4ce9-8149-2c957f8a0245" />
<img width="1465" height="828" alt="Screenshot 2026-04-02 at 3 35 55 AM" src="https://github.com/user-attachments/assets/0826ac53-a1d8-481e-aba5-a37458cd696d" />
<img width="1466" height="679" alt="Screenshot 2026-04-02 at 3 35 44 AM" src="https://github.com/user-attachments/assets/716360ca-f1af-4bb9-870c-a0b574baaacd" />

---




