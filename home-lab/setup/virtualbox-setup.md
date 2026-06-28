
Lab Setup:
# 🏠 Home Lab — Kali + Lubuntu

**Built:** May 2026  
**Purpose:** Practice attacking and defending 
in a safe isolated environment

---

## 🖥️ Lab Setup

| VM | Role | IP |
|---|---|---|
| Kali Linux 2026.1 | Attacker 🐉 | 10.0.2.3 |
| Lubuntu 26.04 | Victim 🐧 | 10.0.2.4 |

**Host machine:** Dell Inspiron 15 3520 (8GB RAM)  
**Hypervisor:** Oracle VirtualBox  
**Network:** NAT Network (LabNet - 10.0.2.0/24)

---

## ⚙️ Tools Used
- VirtualBox + Extension Pack
- Kali Linux (pre-built VM image)
- Lubuntu 26.04 (installed from ISO)

---

## 📋 What I Did
- Created isolated NAT Network (LabNet)
- Configured both VMs on same network
- Confirmed connectivity via ping
- Both VMs can communicate ✅

---

## 🔥 Challenges Faced

### 1. Forgot Lubuntu sudo password
- **Problem:** Set password during install,
  forgot it immediately 😭
- **Fix:** Booted into GRUB recovery mode
  (spammed Esc on boot → Advanced options 
  → recovery mode → root shell)
- **Command used:** `passwd chandu`
- **Lesson:** Write passwords down. Always. 😭

### 2. Ping failing between VMs
- **Problem:** Destination Host Unreachable
- **Fix:** Disabled UFW firewall on Lubuntu
- **Command:** `sudo ufw disable`
- **Lesson:** Default firewall blocks ICMP

---

## ✅ Lab Confirmed Working
