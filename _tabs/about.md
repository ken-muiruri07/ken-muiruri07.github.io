---
title: About
icon: fas fa-info-circle
order: 4
---


## Hello! I am Ken Muiruri.
I’m a developer with a growing focus on cybersecurity, driven by curiosity about how systems really work beneath the surface. I’m especially interested in the space where logic, behavior, and vulnerability intersect, where small oversights can lead to big consequences.

I approach learning by doing: experimenting with tools, breaking things, and understanding why they break. Whether it’s network analysis, system enumeration, or web vulnerabilities, I enjoy the process as much as the outcome.

Beyond tech, I’m drawn to complex stories, films, and music that explore human nature and perspective because in a way, cybersecurity is about understanding people just as much as systems.

## 🎓 Education
#### Kenyatta University, Nairobi, Kenya. 
BSc Mathematics and Computer Science. 
Graduated: July 2025

Relevant focus: programming, databases, algorithms, and computational problem solving.

#### Anestar Boys High School Bahati, Nakuru, Kenya. 
Kenya Certificate of Secondary education (KCSE) 
January 2016 – November 2019

## 💼 Experience
### Cybersecurity Trainee — Cyber Shujaa Program

- Gained hands-on experience in network security, system enumeration, and vulnerability analysis
- Worked with tools such as Nmap and Wireshark
- Completed multiple lab-based security challenges

## 🛠 Skills

### Cybersecurity

- Network Scanning (Nmap)
- Traffic Analysis (Wireshark)
- Enumeration & Reconnaissance
- Basic Web Vulnerability Testing

### Development

- Python
- Django
- HTML, CSS, JavaScript

### Tools

- Linux (Kali)
- Git & GitHub
- Burp Suite

## 🚀 PROJECTS
### 🔍 Project 1 — Automated Network Reconnaissance Toolkit

Developed a Python-based reconnaissance toolkit that automates network scanning, service detection, and basic enumeration using Nmap. The tool parses scan results and highlights potentially vulnerable services for further investigation.

#### Tools: Python, Nmap, Linux
#### Key Features:

- Automated port scanning and service version detection
- Output parsing for readable vulnerability insights
- Modular design for extending enumeration capabilities

#### Key Learnings:

- Deep understanding of TCP/IP and port behavior
- Importance of reconnaissance in attack surface mapping
- Translating raw scan data into actionable intelligence

### 🌐 Project 2 — Secure Web Application (Django)

Designed and developed a Django-based web application with a focus on secure coding practices and user authentication. Implemented measures to mitigate common web vulnerabilities such as SQL injection and cross-site scripting (XSS).

#### Tools: Django, Python, SQLite/PostgreSQL
#### Key Features:

- Secure authentication and session management
- Input validation and sanitization
- Structured backend architecture following MVC principles

#### Key Learnings:

- Secure-by-design development approach
- Common web attack vectors and their mitigation
- Bridging the gap between development and security

### 🧠 Project 3 — Static Malware Analysis & Behavioral Profiling

Performed static analysis on a suspicious executable to identify its structure, embedded strings, and potential behavior without execution. Focused on understanding indicators of compromise and reverse engineering fundamentals.

Tools: IDA Freeware, Strings, Hex analysis

#### Key Features:

- Binary inspection and disassembly
- Identification of suspicious API calls and hardcoded strings
- Behavioral inference based on static indicators

#### Key Learnings:

- Fundamentals of reverse engineering
- Recognizing malicious patterns in binaries
- Importance of safe analysis environments

## 🧪 LAB CHALLENGES

### 🔐 Lab — Sweettooth Inc.

Platform: TryHackMe

#### 🎯 Objective

Perform enumeration, extract sensitive data from databases, gain initial access, and escalate privileges to obtain root-level access on the target system.

#### 🧠 Approach

- Began with database enumeration, identifying available databases and extracting stored information. Queried multiple datasets to uncover operational data and credentials.

- Discovered user credentials within a database, which were then leveraged to gain SSH access to the target system.

- After establishing initial access, conducted system enumeration to identify privilege escalation vectors. Discovered an exposed Docker API running locally, which became the primary escalation path.

- Leveraged the Docker API to execute commands within a running container, ultimately mounting the host filesystem and accessing sensitive files.

#### 🛠 Tools Used

- InfluxDB queries
- SSH
- Docker API (via curl)
- Linux commands

#### 💥 Exploitation

Initial Access

- Extracted credentials from a database and used them to authenticate via SSH, gaining a foothold on the system.

Privilege Escalation

- Identified an exposed Docker API bound to localhost.

- Used port forwarding to interact with the Docker service remotely and enumerate running containers.

- Created and executed commands within a container to:

- Mount the host filesystem

- Traverse sensitive directories

- Locate and read protected files

#### 🔍 Key Findings
- Sensitive credentials stored in accessible databases
- Misconfigured Docker API with insufficient access controls
- Ability to execute commands within containers
- Host filesystem exposure through container misconfiguration
#### 🏁 Outcome

- Successfully gained user-level access via SSH and escalated privileges by exploiting Docker misconfigurations, ultimately retrieving root-level flags from the host system.

#### 📚 Key Lessons
- Poorly secured databases can expose critical credentials
- Docker misconfigurations can lead to full host compromise
- Container escape techniques are powerful in post-exploitation
- Privilege escalation often relies on chaining multiple small weaknesses
