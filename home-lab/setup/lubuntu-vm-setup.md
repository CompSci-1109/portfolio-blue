
# 🐧 Lubuntu VM Setup

**Version:** Lubuntu 26.04 LTS
**Role:** Vulnerable target machine
**RAM:** 768 MB
**CPU:** 1 core
**Storage:** 25 GB
**Network:** NAT Network (LabNet)
**IP:** Dynamic (check with `ip a` each session)

## How I set it up
- Downloaded Lubuntu 26.04 ISO from lubuntu.me
- Created new VM in VirtualBox manually
- Installed Lubuntu from ISO
- Changed network to NAT Network (LabNet)

## Credentials
- Username: `chandu`
- ⚠️ never push actual passwords to GitHub!

## Challenges faced
- Black screen after install → fixed by resetting VM
- Forgot sudo password → recovered via GRUB 
  recovery mode (spammed Esc on boot → 
  Advanced options → root shell → `passwd chandu`)

## First thing I ran
```bash
ip a
# confirms VM is on LabNet
```

## Status
- ✅ installed and running
- ✅ communicating with Kali via `ping`
- ✅ SSH server installed
```
