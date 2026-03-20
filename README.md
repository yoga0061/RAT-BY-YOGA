<div align="center">

# 🛡️ YogaRAT — Remote Access Trojan (Educational)

### CTF & Cybersecurity Learning Project

[![Educational](https://img.shields.io/badge/Purpose-Educational%20Only-blue?style=for-the-badge)]()
[![CTF](https://img.shields.io/badge/Category-CTF%20%2F%20Malware%20Analysis-red?style=for-the-badge)]()
[![License](https://img.shields.io/badge/License-Educational%20Use%20Only-yellow?style=for-the-badge)]()
[![Author](https://img.shields.io/badge/Author-Yoganandha-green?style=for-the-badge)]()

> ⚠️ **This tool was developed strictly for educational, research, and CTF purposes. Misuse is strictly prohibited.**

</div>

---

## 👨‍💻 About the Author

**Yoganandha**  
B.Tech Cybersecurity Student  
*Building offensive tools to better understand defensive security — because you can't defend what you don't understand.*

---

## 📌 Project Overview

**YogaRAT** is a custom-built **Remote Access Trojan (RAT)** developed as part of a hands-on cybersecurity learning journey. This project was created to understand how RATs operate at a technical level — including their communication mechanisms, persistence techniques, and detection vectors — in order to strengthen defensive knowledge and CTF problem-solving skills.

> 💡 *Understanding attacker tools is a core skill in malware analysis, incident response, and red team training.*

---

## ⚙️ Features

- 🔗 **Remote Command Execution** — Execute shell commands on the target machine
- 📁 **File Transfer** — Upload and download files between attacker and target
- 🖥️ **System Reconnaissance** — Gather system info (OS, hostname, user, IP)
- 🔄 **Persistent Connection** — Reconnect mechanism if the session drops
- 🕵️ **Stealth Techniques** — Basic evasion for research and analysis understanding

---

## 🧰 Technical Details

| Component | Details |
|-----------|---------|
| 🐍 **Language** | Python |
| 🌐 **Protocol** | TCP Socket Communication |
| 🖥️ **Target Platform** | Windows / Linux |
| 🔒 **Connection** | Reverse Shell Architecture |
| 🧪 **Test Environment** | Isolated VM / Lab only |

---

## 📂 Repository Structure

```
yogarat/
│
├── server/
│   └── server.py          # Attacker-side listener & control panel
│
├── client/
│   └── client.py          # RAT agent (runs on target machine)
│
├── utils/
│   └── helpers.py         # Shared utilities
│
├── docs/
│   └── analysis.md        # Behavioral analysis & detection notes
│
└── README.md
```

---

## 📦 Releases / Download (Defensive Use Only)

Check the [Releases](../../releases) section to download packaged versions intended **only for defensive analysis and research**.

> 🚫 Do **not** install or run any downloaded binaries on personal or production devices.

---

## 🚀 Usage (Lab Environment Only)

```bash
# 1. Clone the repository
git clone https://github.com/yoga0061/yogarat.git
cd yogarat

# 2. Install dependencies
pip install -r requirements.txt

# 3. Start the server (attacker machine / listener)
python server/server.py

# 4. Run the client (on isolated VM target only)
python client/client.py
```

> ⚠️ **Only run in a fully isolated, disposable lab environment (VM with snapshots, segmented network).**

---

## 🔍 Detection & Defense

Part of the learning goal of YogaRAT is understanding how such tools are **detected and mitigated**. Key detection indicators include:

- Unusual outbound TCP connections on non-standard ports
- Processes spawning unexpected child processes (e.g. `cmd.exe`, `bash`)
- High-frequency beaconing patterns in network traffic
- Persistence registry keys or cron job modifications
- AV/EDR signature triggers on known RAT patterns

---

## ⚠️ Disclaimer

This project exists **strictly for educational, defensive, and research purposes** — including malware analysis, detection engineering, incident response training, and academic study.

The creator **does not support, endorse, or take responsibility** for any misuse of the materials in this repository, including hacking, unauthorized access, distribution, or malicious activity.

**By downloading or using files from this repository, you agree to all of the following:**

- ✅ Use files **only** in a controlled, isolated lab environment (e.g., disposable VM with snapshots, segmented network)
- ✅ **Never** run suspicious binaries on production systems, personal devices, or public networks
- ✅ Follow all applicable **laws, institutional policies, and ethical guidelines**
- ✅ **Notify** the maintainers and your CSIRT/CERT immediately if you discover live malicious infrastructure or unexpected behavior

For questions or to report suspicious findings, contact: **naistam63@gmail.com**

---

## 📜 License

**Educational Use Only**

This project is made available for **educational and research purposes only**. You may study, analyze, and reference this code in academic or lab contexts. Redistribution, commercial use, or deployment against any system without explicit written permission is strictly prohibited.

© 2024 Yoganandha — All rights reserved for non-educational use.

---

<div align="center">

*Built to learn. Not to harm.*

**🛡️ Stay ethical. Stay curious.**

</div>
