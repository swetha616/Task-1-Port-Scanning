# 🛡️ Task 1: Scan Your Local Network for Open Ports

## 🎯 Objective
To discover open ports on devices in the local network to understand network exposure and basic reconnaissance using `nmap`.

---

## 🧰 Tools Used
- **Nmap**: Network Mapper for port scanning
- **Kali Linux VM**: Environment used for scanning

---

## 📝 Steps Performed

### 1. Identified Local IP Range
- Ran `ip a` inside Kali VM
- Local IP: `192.168.174.128/24`
- Network range scanned: `192.168.174.0/24`

### 2. Performed TCP SYN Scan
nmap -sS 192.168.174.128/24


## 📊 Scan Summary

| IP Address         | Status | Open Ports | Service   | MAC Vendor |
|--------------------|--------|------------|-----------|------------|
| `192.168.174.1`    | Up     | None       | —         | VMware     |
| `192.168.174.2`    | Up     | 53/tcp     | DNS       | VMware     |
| `192.168.174.254`  | Up     | None       | —         | VMware     |
| `192.168.174.128`  | Up     | None       | —         | VMware     |


✅ 4 hosts were detected as live.  
Only one device (`192.168.174.2`) had an open port: **53 (DNS)**.


## How to Reproduce This Scan

You can reproduce this scan using:

nmap -sS 192.168.174.128/24 -oN scan_results.txt

Replace 192.168.174.128/24 with your own local subnet.
