# Task 1: Scan Your Local Network for Open Ports

## 🔍 Objective
To discover open ports on devices within the local network and understand network exposure using `nmap`.

---

## 🛠️ Tools Used
- `nmap` (Network Mapper)
- Kali Linux VM

---

## 🧾 Steps Performed

1. **Identified Local IP Range:**
   - Ran `ip a` inside the Kali VM.
   - Found local IP: `192.168.174.128`
   - Used subnet `/24`, so IP range scanned: `192.168.174.0/24`

2. **Performed TCP SYN Scan using Nmap:**
   ```bash
   nmap -sS 192.168.174.128/24
