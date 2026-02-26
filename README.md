# 🛡️ SSH Honeypot Lab – Cowrie

## 📌 Project Overview

This project demonstrates the deployment of a high-interaction SSH honeypot using **Cowrie** on Kali Linux.  
The honeypot simulates a vulnerable SSH server to capture and analyze attacker behavior, login attempts, and executed commands.

The objective of this lab is to understand real-world attack patterns and practice threat monitoring techniques used in Blue Team operations.

---

## 🎯 Objectives

- Deploy an SSH honeypot using Cowrie
- Simulate brute-force login attempts
- Capture attacker commands
- Analyze session logs
- Understand attacker behavior

---

## 🛠️ Tools & Technologies Used

- Kali Linux
- Python 3
- Cowrie Honeypot
- OpenSSH
- Git & GitHub

---

## 📁 Project Structure
Honeypot-Lab
├── cowrie/ # Cowrie honeypot source
├── screenshots/ # Demo screenshots
├── logs/ # Captured logs
├── report/ # Project documentation
├── docs/ # Additional notes
└── README.md

---

## ⚙️ Installation & Setup

### 1️⃣ Clone Repository
git clone https://github.com/SandeepTech06/Honeypot-Lab.git
cd Honeypot-Lab/cowrie

2️⃣ Create Virtual Environment
python3 -m venv cowrie-env
source cowrie-env/bin/activate

3️⃣ Install Dependencies
pip install -r requirements.txt
pip install -e .

4️⃣ Configure Cowrie
cp etc/cowrie.cfg.dist etc/cowrie.cfg

5️⃣ Start Honeypot
cowrie start
Check status:
cowrie status

---

🧪 Attack Simulation
Simulate an SSH attack:
ssh root@localhost -p 2222

Enter random passwords such as:
123456
admin
password

---

📊 Log Monitoring
To view real-time logs: tail -f var/log/cowrie/cowrie.log
Example log output:
New connection from 127.0.0.1
login attempt [root/123456]
CMD: ls
CMD: whoami
CMD: history
