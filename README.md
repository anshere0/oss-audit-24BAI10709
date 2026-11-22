# 🐧 Linux System Administration & Open Source Audit Suite

**Automated POSIX Shell Scripts for Linux System Health Auditing, Package Verification, Log Parsing, and Permission Diagnostics**

[![Platform](https://img.shields.io/badge/OS-Linux%20%2F%20WSL-E95420?style=for-the-badge&logo=linux&logoColor=white)](https://ubuntu.com/)
[![Shell](https://img.shields.io/badge/Language-POSIX_Bash_Scripting-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)](https://www.gnu.org/software/bash/)
[![Coursework](https://img.shields.io/badge/Audit_Focus-Python_3_FOSS-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)

---

## 📌 Overview

This project presents a structured technical audit of **Python as Open Source Software**, evaluating its governance, licensing models, release engineering cycles, and real-world system integrations on Linux.

It pairs theoretical analysis with **five production-grade Bash automation scripts** designed for system administrators to audit host identity, verify package integrity, scan directory security permissions, analyze system logs, and generate interactive compliance reports.

**Author**: Ansh Arora  
**Registration Number**: 24BAI10709  

---

## 📜 Shell Scripts Specification

| Script | Title | Description | Core Linux Commands Used |
|---|---|---|---|
| **`script1.sh`** | **System Identity Report** | Gathers host kernel version, OS distribution, active user, home directory, and formatted system uptime. | `uname`, `lsb_release`, `whoami`, `uptime` |
| **`script2.sh`** | **FOSS Package Inspector** | Queries the Debian package database (`dpkg`) to verify whether Python 3 is installed, extracting exact versioning, architecture, and package description. | `dpkg -l`, `grep`, `cut` |
| **`script3.sh`** | **Disk & Permission Auditor** | Iterates through critical system paths (`/etc`, `/var/log`, `/home`, `/usr/bin`, `/tmp`), extracting user/group ownership, octal permissions, and directory size. | `stat`, `ls -ld`, `du -sh` |
| **`script4.sh`** | **Log File Analyzer** | Parses `/var/log/syslog` or any target log file with custom search keywords (`error`, `fail`, `warn`), counting occurrences and extracting timestamped failure frames. | `grep -i`, `wc -l`, `tail` |
| **`script5.sh`** | **Manifesto Generator** | Interactive CLI prompt collecting user inputs on open-source philosophy, outputting a timestamped Markdown governance document. | `read`, `date`, `cat << EOF` |

---

## 📂 Repository Contents

```text
oss-audit-24BAI10709/
├── Open source audit.pdf       # Comprehensive written audit report (licensing, PEP governance, CPython runtime)
├── script1.sh                  # System Identity Reporter
├── script2.sh                  # FOSS Package Inspector
├── script3.sh                  # Security & Directory Permission Auditor
├── script4.sh                  # System Log Anomaly Scanner
├── script5.sh                  # Interactive Open Source Manifesto Generator
└── README.md
```

---

## 🚀 Execution Guide (Linux / WSL)

### 1. Requirements
- Any Linux environment (Ubuntu 20.04+, Debian, Fedora) or **Windows Subsystem for Linux (WSL)**.
- Bash shell (`/bin/bash`).

### 2. Run Scripts

```bash
# Clone the repository
git clone https://github.com/anshere0/oss-audit-24BAI10709.git
cd oss-audit-24BAI10709

# Grant execution permissions
chmod +x script*.sh

# 1. Run System Identity Report
./script1.sh

# 2. Inspect Python3 Package
./script2.sh

# 3. Audit Critical Directory Permissions
./script3.sh

# 4. Analyze System Logs (Pass target log file and keyword)
./script4.sh /var/log/syslog error

# 5. Generate Open Source Manifesto
./script5.sh
```

---

## 👤 Author
**Ansh Arora**  
- Registration Number: 24BAI10709  
- GitHub: [@anshere0](https://github.com/anshere0)  
- LinkedIn: [Ansh Arora](https://www.linkedin.com/in/ansh-arora0/)
