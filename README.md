# 🔎 Network Scanning using Nmap

## 📌 Project Overview

This project demonstrates network scanning using Nmap on a Linux system.

The project covers:

1. Host Discovery
2. Port Scanning
3. Service & Version Detection
4. OS Detection
5. NSE Script Scanning
6. Firewall Detection
7. Scan Report

---

## 🎯 Objective

The objective of this project is to understand how Nmap can be used to perform network discovery, port scanning, service identification, operating system detection, NSE script scanning, and firewall
analysis.

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| Nmap | Network Scanning |
| Linux | Testing Environment |
| Terminal | Command Execution |

---

## 🧪 Lab Environment

**Operating System:** Linux

**Tool:** Nmap

**Target:** `127.0.0.1`

The localhost address was used for controlled testing.

---

# 1️⃣ Nmap Installation

## Command

```bash
sudo apt update
sudo apt install nmap -y
```
**Description:**
Nmap was installed on the Linux system.

# 2️⃣ Host Discovery

## Command

```bash
nmap -sn 127.0.0.1
```
**Description:**
The -sn option performs host discovery without performing a traditional port scan. It is used to determine whether the target host is available.

# 3️⃣ Port Scanning

## Command

```bash
sudo nmap -p- 127.0.0.1
```
**Description:**
The -p- option scans all TCP ports from 1 through 65535. The scan helps identify open, closed, and filtered ports.

# 4️⃣ Service & Version Detection

## Command

```bash
sudo nmap -sV 127.0.0.1
```
**Description:**
The -sV option attempts to identify services running on open ports and obtain available version information.

# 5️⃣ OS Detection

## Command

```bash
sudo nmap -O 127.0.0.1
```
**Description:**
The -O option attempts to identify the operating system of the target. OS detection may be limited when scanning localhost.

# 6️⃣ NSE Script Scanning

## Command

```bash
sudo nmap -sC -sV 127.0.0.1
```
**Description:**
The -sC option runs Nmap's default NSE scripts. The -sV option performs service and version detection. This provides additional information about detected services.

# 7️⃣ Firewall Detection

## Command

```bash
sudo nmap -sA 127.0.0.1
```
**Description:**
The -sA option performs an ACK scan. The scan can be used to analyze packet-filtering behavior and identify filtered or unfiltered responses.

# 8️⃣ Final Nmap Scan

## Command

```bash
sudo nmap -sC -sV -O 127.0.0.1
```
**Description:**
The final scan combines:

- Default NSE scripts
- Service and version detection
- OS detection

This provides a consolidated view of the target.
