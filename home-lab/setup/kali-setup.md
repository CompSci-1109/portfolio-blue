# 🐉 Kali Linux VM Setup

**Version:** Kali 2026.1
**Role:** Attacker machine
**RAM:** 2048 MB
**CPU:** 2 cores
**Storage:** 80 GB
**Network:** NAT Network (LabNet)
**IP:** 10.0.2.3 (check with `ip a`)

## How I set it up:
- Downloaded pre-built VirtualBox image (.7z) 
  from kali.org
- Extracted using 7-Zip
- Opened .vbox file directly in VirtualBox
- Changed network from NAT to NAT Network (LabNet)

## credentials:
Default credentials were used.
- ⚠️ Change these in a real environment!

## First thing I ran
ip a

the IP is set dynamically by the NAT network which we configured to. always check your VM's IP and note it down.
