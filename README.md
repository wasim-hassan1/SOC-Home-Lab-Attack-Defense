# SOC Home Lab: Attack & Defense Simulation

---

## 📌 Table of Contents

1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Network Topology](#network-topology)
4. [Step 1: Setting Up Virtual Machines](#step-1-setting-up-virtual-machines)
5. [Step 2: Installing Splunk for Log Monitoring](#step-2-installing-splunk-for-log-monitoring)
6. [Step 3: Installing Sysmon on Windows 10](#step-3-installing-sysmon-on-windows-10)
7. [Step 4: Generating Malware with msfvenom](#step-4-generating-malware-with-msfvenom)
8. [Step 5: Setting Up a Metasploit Listener](#step-5-setting-up-a-metasploit-listener)
9. [Step 6: Monitoring Logs with Splunk](#step-6-monitoring-logs-with-splunk)
10. [Troubleshooting](#troubleshooting)
11. [Next Steps & Future Improvements](#next-steps--future-improvements)
12. [How to Contribute](#how-to-contribute)
13. [Conclusion](#conclusion)

---

## 📌 Introduction

This project demonstrates the setup of a home lab environment for cybersecurity testing, including:

- **Attacker Machine** → Kali Linux
- **Target Machine** → Windows 10 VM
- **Logging System** → Splunk for monitoring malicious activities

Key activities include:
- Setting up virtual machines
- Installing and configuring Sysmon for log collection
- Deploying malware using `msfvenom`
- Monitoring attacks using Splunk

---

## 🔧 Prerequisites

| Requirement                | Description                                  |
|----------------------------|----------------------------------------------|
| **RAM**                    | At least **16GB** (to run multiple VMs)     |
| **Virtualization Software** | VMware Workstation or VirtualBox            |
| **Operating Systems**       | ISO files for Windows 10 and Kali Linux     |
| **Logging Tools**           | Splunk and Sysmon setup files               |
| **Internet Connection**     | Required for downloading and configuring tools |

---

## 🎬 Network Topology Animation

Click below to view the **interactive network diagram**:

➡️ [View Animation](https://wasim-hassan1.github.io/SOC-Home-Lab-Attack-Defense/network-diagram.html.svg)

📌 *The Kali Linux machine attacks the Windows VM, and logs are collected by Splunk for analysis.*

---

## Step 1: Setting Up Virtual Machines

### 🖥️ 1.1 Install Kali Linux (Attacker Machine)

1. Download **Kali Linux ISO** from [Kali Official Website](https://www.kali.org/downloads/).
2. Create a new VM in VMware/VirtualBox and install Kali Linux.
3. Update and upgrade Kali:
